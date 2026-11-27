# Kumpulan Skills Antigravity IDE - Lenz

Koleksi **45 Agent Skills** untuk **Google Antigravity IDE**, tersusun rapi dalam **7 folder kategori fungsi** agar mudah dipilih, dipelajari, dan dipasang ke ruang kerja baru.

Website: [lenznity.my.id](https://lenznity.my.id)

---

## Struktur Folder Berdasarkan Fungsi

```text
skills/
├── video-remotion/       (15 skills) — Produksi video Remotion & standar TikTok viral
├── anti-slop/            (6 skills)  — Filter desain & kode agar bebas AI slop
├── animasi-interaksi/    (6 skills)  — Motion web/React Native & audit animasi
├── ui-ux-desain/         (9 skills)  — Sistem desain, komponen UI, mobile-native
├── kualitas-kode/        (6 skills)  — Penyederhanaan kode (Ponytail suite)
├── keamanan-dan-bot/     (2 skills)  — Threat modeling & audit bot WhatsApp
└── swift-mobile/         (1 skill)   — Pengembangan Swift modern (Swift 6)
```

---

## Cara Memasang ke Antigravity IDE

### 1. Lewat Prompt (Otomatis)

Buka proyek di **Antigravity IDE**, lalu kirim salah satu prompt berikut ke Agent:

**Untuk proyek saat ini:**
```text
Ambil repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin semua folder skill di dalam `skills/*/*` ke `.agents/skills/` di proyek ini tanpa menghapus skill yang sudah ada.
```

**Untuk semua proyek (global):**
```text
Ambil repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin semua folder skill di dalam `skills/*/*` ke folder global skills (`~/.agents/skills/` di macOS/Linux atau `C:\Users\<Username>\.agents\skills\` di Windows) tanpa menimpa skill yang sudah ada.
```

### 2. Manual (Terminal)

1. Clone repositori:
   ```bash
   git clone https://github.com/Lenzx999/skills-antigravity-ide-lenz.git
   ```
2. Salin seluruh isi `skills/*/*` ke `.agents/skills/` (atau `~/.agents/skills/`):
   - **Windows (PowerShell):**
     ```powershell
     New-Item -ItemType Directory -Force -Path ".agents\skills" | Out-Null
     Get-ChildItem "skills-antigravity-ide-lenz\skills\*\*" -Directory | Copy-Item -Destination ".agents\skills\" -Recurse -Force
     ```
   - **macOS / Linux:**
     ```bash
     mkdir -p ~/.agents/skills && cp -r skills-antigravity-ide-lenz/skills/*/* ~/.agents/skills/
     ```
3. Buka sesi chat baru di Antigravity IDE.

---

## Daftar Lengkap Skills (45 Skills)

### 1. `skills/video-remotion/` (15 Skills)

| Skill | Fungsi |
|---|---|
| [`remotion-best-practices`](skills/video-remotion/remotion-best-practices/SKILL.md) | Router utama seluruh panduan resmi Remotion agar animasi terikat ke frame (`useCurrentFrame()`). |
| [`remotion-tiktok-viral`](skills/video-remotion/remotion-tiktok-viral/SKILL.md) | Standar produksi video TikTok/Reels: safe zone `1080x1920`, render `PNG + CRF 6` bebas blur, audio *auto-ducking*, dan kepatuhan moderasi TikTok. |
| [`remotion-create`](skills/video-remotion/remotion-create/SKILL.md) | Panduan inisialisasi proyek Remotion baru beserta aturan tata letak video. |
| [`remotion-markup`](skills/video-remotion/remotion-markup/SKILL.md) | Aturan inti penulisan komponen React Remotion, transisi, audio, dan efek visual. |
| [`remotion-elements`](skills/video-remotion/remotion-elements/SKILL.md) | Cara memasang dan menyesuaikan komponen video siap pakai dari pustaka Remotion Elements. |
| [`remotion-captions`](skills/video-remotion/remotion-captions/SKILL.md) | Menampilkan, menyinkronkan, dan mengimpor subtitle/caption kata per kata (SRT dan transkripsi). |
| [`remotion-interactivity`](skills/video-remotion/remotion-interactivity/SKILL.md) | Struktur timeline agar komposisi dan aset bisa diedit langsung di Remotion Studio. |
| [`remotion-maps`](skills/video-remotion/remotion-maps/SKILL.md) | Pembuatan animasi peta, rute, dan marker menggunakan Mapbox, MapLibre, dan GeoJSON. |
| [`remotion-multimedia`](skills/video-remotion/remotion-multimedia/SKILL.md) | Mengolah media di browser serta membaca durasi dan dimensi audio/video. |
| [`remotion-render`](skills/video-remotion/remotion-render/SKILL.md) | Panduan render video MP4, gambar still, frame transparan, dan ekspor timeline. |
| [`remotion-saas`](skills/video-remotion/remotion-saas/SKILL.md) | Integrasi Remotion Player dan rendering ke dalam aplikasi SaaS / web framework. |
| [`remotion-studio`](skills/video-remotion/remotion-studio/SKILL.md) | Menjalankan dan mengoperasikan preview Remotion Studio saat pengembangan video. |
| [`remotion-docs`](skills/video-remotion/remotion-docs/SKILL.md) | Akses rujukan dokumentasi resmi Remotion untuk kebutuhan teknis lanjutan. |
| [`remotion-license`](skills/video-remotion/remotion-license/SKILL.md) | Panduan konfigurasi lisensi Remotion pada proses render produksi maupun proyek gratis. |
| [`remotion-upgrade`](skills/video-remotion/remotion-upgrade/SKILL.md) | Langkah pembaruan versi paket Remotion agar tetap sinkron dan bebas konflik. |

### 2. `skills/anti-slop/` (6 Skills)

| Skill | Fungsi |
|---|---|
| [`antislop`](skills/anti-slop/antislop/SKILL.md) | Filter inti anti AI slop untuk menjaga arah desain tetap punya karakter dan tujuan jelas. |
| [`antislop-ui`](skills/anti-slop/antislop-ui/SKILL.md) | Aturan visual, warna murni, tata letak, dan motion agar UI/video tidak terlihat template AI. |
| [`antislop-code`](skills/anti-slop/antislop-code/SKILL.md) | Filter kualitas kode frontend/komponen agar ringkas dan bebas abstraksi berlebihan. |
| [`antislop-copywriting`](skills/anti-slop/antislop-copywriting/SKILL.md) | Menjaga teks UI/judul tetap lugas, manusiawi, dan bebas frasa generik AI. |
| [`antislop-human`](skills/anti-slop/antislop-human/SKILL.md) | Pemeriksaan aksesibilitas, kontras WCAG, dan keterbacaan manusia nyata. |
| [`antislop-layoutmobile`](skills/anti-slop/antislop-layoutmobile/SKILL.md) | Standar tata letak responsif ponsel agar nyaman dipakai di layar kecil. |

### 3. `skills/animasi-interaksi/` (6 Skills)

| Skill | Fungsi |
|---|---|
| [`animate`](skills/animasi-interaksi/animate/SKILL.md) | Merancang dan menulis kode animasi web yang tepat guna, kurva, dan durasi ideal. |
| [`animate-expo`](skills/animasi-interaksi/animate-expo/SKILL.md) | Membangun animasi React Native & Expo (Reanimated, Gesture Handler, Haptics) yang mulus. |
| [`animation-vocabulary`](skills/animasi-interaksi/animation-vocabulary/SKILL.md) | Kamus istilah teknis animasi dari deskripsi efek gerak sehari-hari. |
| [`find-animation-opportunities`](skills/animasi-interaksi/find-animation-opportunities/SKILL.md) | Memindai kode untuk menemukan bagian yang layak dianimasikan dan menahan yang tidak perlu. |
| [`improve-animations`](skills/animasi-interaksi/improve-animations/SKILL.md) | Mengaudit kode animasi dan menyusun rencana perbaikan terprioritas secara *read-only*. |
| [`review-animations`](skills/animasi-interaksi/review-animations/SKILL.md) | Meninjau kode animasi dan transisi agar tetap ringan, responsif, dan tepat sasaran. |

### 4. `skills/ui-ux-desain/` (9 Skills)

| Skill | Fungsi |
|---|---|
| [`apple-design`](skills/ui-ux-desain/apple-design/SKILL.md) | Prinsip desain antarmuka dan gerak fisik ala Apple untuk web (gestur, pegas, tipografi). |
| [`ask-sonner`](skills/ui-ux-desain/ask-sonner/SKILL.md) | Panduan setup, styling, theming, dan debugging library toast **Sonner** di React. |
| [`break-ui`](skills/ui-ux-desain/break-ui/SKILL.md) | Menguji ketahanan komponen UI dengan data ekstrem (teks panjang, angka besar, data kosong). |
| [`design-dna`](skills/ui-ux-desain/design-dna/SKILL.md) | Mengekstrak token desain, gaya visual, dan efek grafis (Canvas/WebGL/3D) dari referensi ke JSON. |
| [`emil-design-eng`](skills/ui-ux-desain/emil-design-eng/SKILL.md) | Standar *design engineering* untuk kehalusan komponen, interaksi, dan detail antarmuka. |
| [`mobile-native`](skills/ui-ux-desain/mobile-native/SKILL.md) | Perbaikan CSS dan meta tag agar web terasa seperti aplikasi native di ponsel. |
| [`pick-ui-library`](skills/ui-ux-desain/pick-ui-library/SKILL.md) | Rekomendasi library frontend terkurasi (dialog, toast, grafik, command menu, drag-and-drop). |
| [`prototype`](skills/ui-ux-desain/prototype/SKILL.md) | Membangun beberapa variasi UI berbeda sekaligus lengkap dengan pemilih tampilan. |
| [`ui-ux-pro-max`](skills/ui-ux-desain/ui-ux-pro-max/SKILL.md) | Referensi desain UI/UX lengkap dengan skrip pencarian lokal (gaya, palet, font, ikon). |

### 5. `skills/kualitas-kode/` (6 Skills)

| Skill | Fungsi |
|---|---|
| [`ponytail`](skills/kualitas-kode/ponytail/SKILL.md) | Mengarahkan agent memilih solusi paling sederhana, minimal, dan langsung jalan (`lite`, `full`, `ultra`). |
| [`ponytail-audit`](skills/kualitas-kode/ponytail-audit/SKILL.md) | Audit proyek untuk memangkas kode berbelit-belit dan dependensi yang tidak perlu. |
| [`ponytail-debt`](skills/kualitas-kode/ponytail-debt/SKILL.md) | Mengumpulkan semua komentar `ponytail:` di kode menjadi daftar utang teknis. |
| [`ponytail-gain`](skills/kualitas-kode/ponytail-gain/SKILL.md) | Menampilkan ringkasan penghematan kode dari penggunaan mode `ponytail`. |
| [`ponytail-help`](skills/kualitas-kode/ponytail-help/SKILL.md) | Referensi cepat perintah dan mode `ponytail`. |
| [`ponytail-review`](skills/kualitas-kode/ponytail-review/SKILL.md) | Meninjau perubahan kode khusus untuk mendeteksi bagian yang terlalu rumit. |

### 6. `skills/keamanan-dan-bot/` (2 Skills)

| Skill | Fungsi |
|---|---|
| [`threat-model`](skills/keamanan-dan-bot/threat-model/SKILL.md) | Pemodelan ancaman keamanan desain aplikasi (STRIDE, PASTA, LINDDUN, risiko privasi). |
| [`whatsapp-bot-deep-audit`](skills/keamanan-dan-bot/whatsapp-bot-deep-audit/SKILL.md) | Protokol audit dan pengujian fitur bot WhatsApp (Baileys) untuk pesan teks, media, dan fallback unduhan. |

### 7. `skills/swift-mobile/` (1 Skill)

| Skill | Fungsi |
|---|---|
| [`write-swift`](skills/swift-mobile/write-swift/SKILL.md) | Panduan menulis kode Swift modern (Swift 6.x, *value types*, *concurrency*, `actor`, Swift Testing). |

---

## Kredit & Atribusi

Seluruh hak cipta tetap menjadi milik pembuat masing-masing:

- **Kelompok `video-remotion`**: Resmi dari **Remotion** ([github.com/remotion-dev/skills](https://github.com/remotion-dev/skills)), ditambah `remotion-tiktok-viral` oleh **Lenz**.
- **Kelompok `anti-slop`**: **Anti-Slop** oleh **Miqdad Badjuber** ([github.com/miqdadbadjuber/anti-slop](https://github.com/miqdadbadjuber/anti-slop)).
- **Kelompok `animasi-interaksi` & `ui-ux-desain`**: Filosofi *design engineering* **Emil Kowalski** ([animations.dev](https://animations.dev/) / [sonner.emilkowal.ski](https://sonner.emilkowal.ski/)), **UI/UX Pro Max**, dan koleksi komunitas AI Agent.
- **Kelompok `kualitas-kode`**: **Ponytail Skill Suite** (Lisensi MIT).
- **`threat-model`**: **Grim Prompter** (*Threat Modeling Skill*).
- **`whatsapp-bot-deep-audit`**: Dibuat oleh **Lenz**.
