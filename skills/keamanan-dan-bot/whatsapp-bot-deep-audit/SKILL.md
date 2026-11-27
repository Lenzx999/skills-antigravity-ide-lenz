---
name: whatsapp-bot-deep-audit
description: >-
  Metodologi audit mendalam, verifikasi logika, dan protokol pengujian runtime multi-payload
  untuk seluruh fitur bot WhatsApp (teks langsung, reply teks, reply gambar, reply video,
  dokumen berkas, dan handling download stream).
---

# Panduan & Protokol Audit Mendalam Fitur Bot WhatsApp

Skill ini diciptakan untuk mencegah kelemahan audit dangkal (*shallow dry-run*) di mana fitur yang membutuhkan media hanya merespons teks petunjuk tanpa pernah menguji alur pengunduhan dan pengolahan media sesungguhnya.

---

## 1. Masalah Kritis Pengujian Media di Baileys
Banyak plugin bot WhatsApp tampak "sehat" saat diuji dengan teks biasa karena berhenti di baris pengecekan awal:
```js
if (!m.quoted && !text) return m.reply('Kirim/balas media...');
```
Namun saat digunakan oleh pengguna nyata di WhatsApp:
1. **Reply Media Mengirim `extendedTextMessage`**: Pesan yang masuk bertipe teks, sedangkan data media berada di dalam `m.msg.contextInfo.quotedMessage`.
2. **`mimetype` Tersembunyi**: Pada pesan media terenkripsi, ephemeral, atau view-once, properti `mimetype` sering kali tidak berada di root `m.quoted.msg`, melainkan di sub-kunci proto Baileys.
3. **Download Tanpa Fallback**: Memanggil `lenzx.downloadAndSaveMediaMessage` pada objek `qmsg` yang tidak lengkap dapat melempar exception atau menghasilkan buffer kosong.

---

## 2. Standar Koding Wajib untuk Semua Fitur Media (Anti-Gagal Reply)

Setiap fitur yang memproses media (foto, video, audio, dokumen) **WAJIB** menerapkan arsitektur berikut:

### A. Deteksi Multi-Layer (Anti "Dibilang Belum Reply")
```js
const quoted = m.quoted ? m.quoted : m;
let targetMsg = m.quoted ? m.quoted : (qmsg || m);
if (m.quoted && typeof m.getQuotedObj === 'function') {
    try {
        const qObj = await m.getQuotedObj();
        if (qObj) targetMsg = qObj;
    } catch (_) {}
}

const targetInner = targetMsg?.msg || targetMsg?.message || targetMsg;
const rawMime = String((targetInner?.mimetype || targetMsg?.mimetype || mime || quoted?.mime || quoted?.mimetype || '')).toLowerCase();
const rawFileName = String((targetInner?.fileName || targetMsg?.fileName || quoted?.fileName || targetInner?.filename || targetMsg?.filename || '')).toLowerCase();
const msgType = String(m.type || quoted?.type || targetMsg?.type || '').toLowerCase();

const isDoc = msgType.includes('document') || rawMime.includes('document');
let isImage = /image/.test(rawMime) || /image/i.test(msgType) || /\.(jpe?g|png|webp|heic|bmp)$/i.test(rawFileName);
let isVideo = /video/.test(rawMime) || /video/i.test(msgType) || /\.(mp4|mov|mkv|avi|3gp|webm)$/i.test(rawFileName);
const hasMedia = isImage || isVideo || isDoc || !!rawMime || !!m.quoted?.isMedia;

if (!hasMedia) {
    return m.reply(`Kirim atau balas media dengan perintah ${prefix + command}`);
}
```

### B. Dual/Triple Fallback Pengunduhan Media
```js
let mediaPath = null;
try {
    mediaPath = await lenzx.downloadAndSaveMediaMessage(targetMsg);
} catch (dlErr) {
    // Fallback 1: Coba via qmsg
    if (qmsg && qmsg !== targetMsg) {
        try { mediaPath = await lenzx.downloadAndSaveMediaMessage(qmsg); } catch (_) {}
    }
    // Fallback 2: Unduh buffer langsung
    if (!mediaPath && typeof lenzx.downloadMediaMessage === 'function') {
        const buf = await lenzx.downloadMediaMessage(targetMsg).catch(() => null)
                    || (m.quoted ? await lenzx.downloadMediaMessage(m.quoted).catch(() => null) : null);
        if (buf && buf.length > 0) {
            const ext = isVideo ? '.mp4' : (isImage ? '.jpg' : '.bin');
            const tempFile = path.join('./database/temp', `raw_${Date.now()}_${getRandom(ext)}`);
            fs.writeFileSync(tempFile, buf);
            mediaPath = tempFile;
        }
    }
    if (!mediaPath) throw dlErr;
}
```

---

## 3. Protokol Multi-Skenario Audit Runtime
Saat melakukan audit fitur di workspace ini, pengujian **TIDAK BOLEH** hanya menjalankan skenario teks. Wajib menjalankan 4 skenario simulasi:

1. **Skenario 1 (Tanpa Argumen)**: Mengetes respon petunjuk awal & validasi parameter kosong.
2. **Skenario 2 (Teks Argumen)**: Mengetes parsing query, scraping teks, atau command switch.
3. **Skenario 3 (Quoted Image Media)**: Mengetes respon ketika pengguna me-reply foto (validasi `isMedia`, ekstraksi buffer gambar, dan filter pengolahan).
4. **Skenario 4 (Quoted Video Media)**: Mengetes respon ketika pengguna me-reply video (validasi stream durasi, probing FFprobe, pemotongan, dan filter video).

