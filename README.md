# Kumpulan Skills Antigravity IDE — Lenz

Kumpulan **24 Agent Skills** yang saya pakai sehari-hari di **Google Antigravity IDE**. Semua *skill* di sini disalin dari beberapa proyek pribadi agar mudah dipakai ulang atau dipasang ke proyek baru.

- Website: [https://lenznity.my.id](https://lenznity.my.id)

---

## Cara Memasang ke Antigravity IDE

Ada dua cara memasang *skills* ini: menyuruh Agent Antigravity memasangnya otomatis lewat prompt, atau menyalin foldernya secara manual.

### 1. Lewat Prompt (Otomatis oleh Agent)

Buka proyek kamu di **Antigravity IDE**, lalu salin dan kirim salah satu prompt berikut ke Agent:

**Pasang untuk satu proyek saja:**
```text
Ambil repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin semua folder di dalam direktori `skills/` ke folder `.agents/skills/` di proyek ini. Jangan hapus skill yang sudah ada, dan pastikan seluruh isi tiap folder (termasuk `SKILL.md` dan file pendukungnya) ikut tersalin.
```

**Pasang untuk semua proyek (global):**
```text
Ambil repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin semua folder di dalam direktori `skills/` ke folder global skills Antigravity (`~/.agents/skills/` di macOS/Linux atau `C:\Users\<Username>\.agents\skills\` di Windows). Jangan timpa atau hapus skill lain yang sudah ada.
```

### 2. Cara Manual

1. Clone repositori ini:
   ```bash
   git clone https://github.com/Lenzx999/skills-antigravity-ide-lenz.git
   ```
2. Salin semua folder yang ada di dalam `skills/` ke salah satu lokasi berikut:
   - **Khusus satu proyek:** `<folder-proyek>/.agents/skills/`
   - **Semua proyek (Windows):** `C:\Users\<Username>\.agents\skills\`
   - **Semua proyek (macOS / Linux):** `~/.agents/skills/`
3. Buka sesi chat baru di Antigravity IDE, maka *skills* akan langsung terbaca otomatis.

---

## Daftar Skills & Fungsinya

### Animasi & Kualitas Tampilan (12 Skills)

| Skill | Fungsi |
|---|---|
| [`animate`](skills/animate/SKILL.md) | Membuat animasi web dari nol dengan menentukan apakah elemen memang perlu bergerak, properti yang aman dipakai, serta kurva dan durasi yang pas. |
| [`animate-expo`](skills/animate-expo/SKILL.md) | Membuat animasi di React Native dan Expo (Reanimated, Gesture Handler, `expo-haptics`) agar berjalan mulus di perangkat sungguhan. |
| [`animation-vocabulary`](skills/animation-vocabulary/SKILL.md) | Kamus istilah animasi untuk mencari nama teknis dari efek gerak yang dijelaskan dengan bahasa awam. |
| [`ask-sonner`](skills/ask-sonner/SKILL.md) | Panduan memasang, mengatur tema, dan mengatasi masalah pada library notifikasi toast **Sonner** di React. |
| [`break-ui`](skills/break-ui/SKILL.md) | Menguji ketahanan tampilan dengan data ekstrem (teks sangat panjang, email tanpa spasi, angka besar, data kosong, dan emoji). |
| [`emil-design-eng`](skills/emil-design-eng/SKILL.md) | Panduan merancang komponen dan detail interaksi antarmuka agar terasa rapi dan nyaman dipakai. |
| [`find-animation-opportunities`](skills/find-animation-opportunities/SKILL.md) | Mengecek kode yang ada untuk mencari bagian yang cocok diberi animasi, sekaligus menyaring bagian yang sebaiknya dibiarkan statis. |
| [`improve-animations`](skills/improve-animations/SKILL.md) | Mengaudit kode animasi yang sudah ada dan menyusun daftar rencana perbaikannya tanpa langsung mengubah kode. |
| [`mobile-native`](skills/mobile-native/SKILL.md) | Kumpulan perbaikan CSS dan meta tag agar web terasa seperti aplikasi bawaan di HP (menghilangkan *tap flash*, *sticky hover*, bug `100vh`, area *notch*, dll). |
| [`pick-ui-library`](skills/pick-ui-library/SKILL.md) | Membantu memilih library frontend yang tepat (dialog, toast, grafik, command menu, drag-and-drop, dll). |
| [`prototype`](skills/prototype/SKILL.md) | Membuat beberapa variasi desain komponen UI sekaligus lengkap dengan pemilih tampilan agar bisa dibandingkan langsung. |
| [`review-animations`](skills/review-animations/SKILL.md) | Mengulas kode animasi dan transisi agar gerakannya tetap ringan, cepat, dan tidak mengganggu pengguna. |

### Desain UI/UX & Swift (4 Skills)

| Skill | Fungsi |
|---|---|
| [`apple-design`](skills/apple-design/SKILL.md) | Menerapkan prinsip desain antarmuka dan gerak fisik ala Apple ke web (gestur, efek pegas, transparansi, dan tipografi). |
| [`design-dna`](skills/design-dna/SKILL.md) | Mengekstrak gaya visual, token warna, tipografi, dan efek grafis (Canvas/WebGL/3D) dari referensi desain ke format JSON terstruktur. |
| [`ui-ux-pro-max`](skills/ui-ux-pro-max/SKILL.md) | Panduan desain UI/UX lengkap dengan skrip pencarian lokal (berisi puluhan gaya desain, palet warna, pasangan font, ikon, dan contoh grafik). |
| [`write-swift`](skills/write-swift/SKILL.md) | Panduan menulis kode Swift modern (Swift 6.x, *value types*, keamanan *concurrency*, `actor`, dan Swift Testing). |

### Penyederhanaan Kode — Ponytail (6 Skills)

| Skill | Fungsi |
|---|---|
| [`ponytail`](skills/ponytail/SKILL.md) | Mengarahkan agent agar selalu memilih solusi paling sederhana, singkat, dan langsung jalan tanpa kode berlebih (mode `lite`, `full`, `ultra`). |
| [`ponytail-audit`](skills/ponytail-audit/SKILL.md) | Memindai seluruh proyek untuk mencari kode yang terlalu rumit atau library tambahan yang sebenarnya bisa diganti fitur bawaan. |
| [`ponytail-debt`](skills/ponytail-debt/SKILL.md) | Mengumpulkan semua catatan komentar `ponytail:` di dalam kode menjadi daftar pekerjaan yang ditunda. |
| [`ponytail-gain`](skills/ponytail-gain/SKILL.md) | Menampilkan ringkasan penghematan kode dari penggunaan mode `ponytail`. |
| [`ponytail-help`](skills/ponytail-help/SKILL.md) | Panduan singkat daftar perintah dan mode yang tersedia di `ponytail`. |
| [`ponytail-review`](skills/ponytail-review/SKILL.md) | Meninjau perubahan kode khusus untuk mencari bagian yang berlebihan atau terlalu rumit. |

### Keamanan & Bot WhatsApp (2 Skills)

| Skill | Fungsi |
|---|---|
| [`threat-model`](skills/threat-model/SKILL.md) | Menganalisis celah keamanan desain aplikasi secara menyeluruh (metode STRIDE, PASTA, LINDDUN, serta risiko privasi) dan menyimpannya ke folder `threat-model/`. |
| [`whatsapp-bot-deep-audit`](skills/whatsapp-bot-deep-audit/SKILL.md) | Panduan pengujian dan audit fitur bot WhatsApp (Baileys) untuk pesan teks, balasan gambar/video/dokumen, media sekali lihat, dan penanganan unduhan media. |

---

## Kredit & Pembuat Asli

Repositori ini hanya mengumpulkan *skills* yang saya gunakan. Seluruh hak cipta dan penghargaan tetap milik pembuat aslinya masing-masing:

- **Kelompok Animasi & Design Engineering** (`animate`, `animate-expo`, `animation-vocabulary`, `ask-sonner`, `break-ui`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `mobile-native`, `pick-ui-library`, `prototype`, `review-animations`):
  Berdasarkan filosofi desain dan animasi **Emil Kowalski** ([animations.dev](https://animations.dev/) / [sonner.emilkowal.ski](https://sonner.emilkowal.ski/)).
- **Kelompok Ponytail** (`ponytail`, `ponytail-audit`, `ponytail-debt`, `ponytail-gain`, `ponytail-help`, `ponytail-review`):
  Karya **Ponytail Skill Suite** dengan **Lisensi MIT**.
- **`threat-model`**:
  Bagian dari **Grim Prompter** (*Threat Modeling Skill*).
- **`ui-ux-pro-max`**:
  Karya proyek komunitas **UI/UX Pro Max**.
- **`apple-design`, `design-dna`, `write-swift`**:
  Koleksi *skills* komunitas (nama penulis asli tidak tercantum di dalam berkas sumbernya).
- **`whatsapp-bot-deep-audit`**:
  Dibuat oleh **Lenz** ([lenznity.my.id](https://lenznity.my.id)).

> Jika kamu pembuat asli salah satu *skill* di atas dan ingin menambahkan tautan sumber atau perbaikan kredit, silakan buka *issue* atau hubungi melalui [lenznity.my.id](https://lenznity.my.id).

---

**Website:** [https://lenznity.my.id](https://lenznity.my.id)
