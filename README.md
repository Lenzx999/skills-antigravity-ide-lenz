# Kumpulan Skills Antigravity IDE - Lenz

Koleksi **38 Agent Skills** untuk **Google Antigravity IDE**, dikurasi dari proyek-proyek pribadi agar siap langsung dipasang ke ruang kerja baru.

Website: [lenznity.my.id](https://lenznity.my.id)

---

## Cara Memasang ke Antigravity IDE

### 1. Lewat Prompt (Otomatis)

Buka proyek di **Antigravity IDE**, lalu kirim salah satu prompt berikut ke Agent:

**Untuk proyek saat ini:**
```text
Ambil repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin semua folder di dalam direktori `skills/` ke `.agents/skills/` di proyek ini tanpa menghapus skill yang sudah ada.
```

**Untuk semua proyek (global):**
```text
Ambil repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin semua folder di dalam direktori `skills/` ke folder global skills (`~/.agents/skills/` di macOS/Linux atau `C:\Users\<Username>\.agents\skills\` di Windows) tanpa menimpa skill yang sudah ada.
```

### 2. Manual

1. Clone repositori:
   ```bash
   git clone https://github.com/Lenzx999/skills-antigravity-ide-lenz.git
   ```
2. Salin seluruh folder di dalam `skills/` ke:
   - **Per proyek:** `<folder-proyek>/.agents/skills/`
   - **Global (Windows):** `C:\Users\<Username>\.agents\skills\`
   - **Global (macOS/Linux):** `~/.agents/skills/`
3. Buka sesi chat baru di Antigravity IDE.

---

## Daftar Skills (38 Skills)

### Remotion Video (14)

| Skill | Fungsi |
|---|---|
| [`remotion-best-practices`](skills/remotion-best-practices/SKILL.md) | Router utama seluruh panduan resmi Remotion agar animasi terikat ke frame dan stabil saat render. |
| [`remotion-create`](skills/remotion-create/SKILL.md) | Panduan inisialisasi proyek Remotion baru beserta aturan tata letak video. |
| [`remotion-markup`](skills/remotion-markup/SKILL.md) | Aturan inti penulisan komponen React Remotion, transisi, audio, efek visual, dan `useCurrentFrame()`. |
| [`remotion-elements`](skills/remotion-elements/SKILL.md) | Cara memasang dan menyesuaikan komponen video siap pakai dari pustaka Remotion Elements. |
| [`remotion-captions`](skills/remotion-captions/SKILL.md) | Menampilkan, menyinkronkan, dan mengimpor subtitle/caption kata per kata (SRT dan transkripsi). |
| [`remotion-interactivity`](skills/remotion-interactivity/SKILL.md) | Struktur timeline agar komposisi dan aset bisa diedit langsung di Remotion Studio. |
| [`remotion-maps`](skills/remotion-maps/SKILL.md) | Pembuatan animasi peta, rute, dan marker menggunakan Mapbox, MapLibre, dan GeoJSON. |
| [`remotion-multimedia`](skills/remotion-multimedia/SKILL.md) | Mengolah media di browser serta membaca durasi dan dimensi audio/video. |
| [`remotion-render`](skills/remotion-render/SKILL.md) | Panduan render video MP4, gambar still, frame transparan, dan ekspor timeline. |
| [`remotion-saas`](skills/remotion-saas/SKILL.md) | Integrasi Remotion Player dan rendering ke dalam aplikasi SaaS / web framework. |
| [`remotion-studio`](skills/remotion-studio/SKILL.md) | Menjalankan dan mengoperasikan preview Remotion Studio saat pengembangan video. |
| [`remotion-docs`](skills/remotion-docs/SKILL.md) | Akses rujukan dokumentasi resmi Remotion untuk kebutuhan teknis lanjutan. |
| [`remotion-license`](skills/remotion-license/SKILL.md) | Panduan konfigurasi lisensi Remotion pada proses render produksi maupun proyek gratis. |
| [`remotion-upgrade`](skills/remotion-upgrade/SKILL.md) | Langkah pembaruan versi paket Remotion agar tetap sinkron dan bebas konflik. |

### Animasi & Kualitas Tampilan (12)

| Skill | Fungsi |
|---|---|
| [`animate`](skills/animate/SKILL.md) | Merancang dan menulis kode animasi web yang tepat guna, properti aman, kurva, dan durasi ideal. |
| [`animate-expo`](skills/animate-expo/SKILL.md) | Membangun animasi React Native & Expo (Reanimated, Gesture Handler, Haptics) yang mulus di perangkat nyata. |
| [`animation-vocabulary`](skills/animation-vocabulary/SKILL.md) | Kamus istilah teknis animasi dari deskripsi efek gerak sehari-hari. |
| [`ask-sonner`](skills/ask-sonner/SKILL.md) | Panduan setup, styling, theming, dan debugging library toast **Sonner** di React. |
| [`break-ui`](skills/break-ui/SKILL.md) | Menguji ketahanan komponen UI dengan data ekstrem (teks panjang, email tanpa spasi, angka besar, data kosong, emoji). |
| [`emil-design-eng`](skills/emil-design-eng/SKILL.md) | Standar *design engineering* untuk kehalusan komponen, interaksi, dan detail antarmuka. |
| [`find-animation-opportunities`](skills/find-animation-opportunities/SKILL.md) | Memindai kode untuk menemukan bagian yang layak dianimasikan dan menahan yang tidak perlu. |
| [`improve-animations`](skills/improve-animations/SKILL.md) | Mengaudit kode animasi dan menyusun rencana perbaikan terprioritas secara *read-only*. |
| [`mobile-native`](skills/mobile-native/SKILL.md) | Perbaikan CSS dan meta tag agar web terasa seperti aplikasi native di ponsel (*tap flash*, *sticky hover*, `100vh`, *notch*). |
| [`pick-ui-library`](skills/pick-ui-library/SKILL.md) | Rekomendasi library frontend terkurasi (dialog, toast, grafik, command menu, drag-and-drop). |
| [`prototype`](skills/prototype/SKILL.md) | Membangun beberapa variasi UI berbeda sekaligus lengkap dengan pemilih tampilan untuk dibandingkan langsung. |
| [`review-animations`](skills/review-animations/SKILL.md) | Meninjau kode animasi dan transisi agar tetap ringan, responsif, dan tepat sasaran. |

### Desain UI/UX & Swift (4)

| Skill | Fungsi |
|---|---|
| [`apple-design`](skills/apple-design/SKILL.md) | Prinsip desain antarmuka dan gerak fisik ala Apple untuk web (gestur, pegas, transparansi, tipografi). |
| [`design-dna`](skills/design-dna/SKILL.md) | Mengekstrak token desain, gaya visual, dan efek grafis (Canvas/WebGL/3D) dari referensi ke format JSON. |
| [`ui-ux-pro-max`](skills/ui-ux-pro-max/SKILL.md) | Referensi desain UI/UX lengkap dengan skrip pencarian lokal (gaya desain, palet warna, font, ikon, grafik). |
| [`write-swift`](skills/write-swift/SKILL.md) | Panduan menulis kode Swift modern (Swift 6.x, *value types*, *concurrency*, `actor`, Swift Testing). |

### Penyederhanaan Kode - Ponytail (6)

| Skill | Fungsi |
|---|---|
| [`ponytail`](skills/ponytail/SKILL.md) | Mengarahkan agent memilih solusi paling sederhana, minimal, dan langsung jalan (mode `lite`, `full`, `ultra`). |
| [`ponytail-audit`](skills/ponytail-audit/SKILL.md) | Audit proyek untuk memangkas kode berbelit-belit dan mengganti dependensi yang tidak perlu dengan fitur bawaan. |
| [`ponytail-debt`](skills/ponytail-debt/SKILL.md) | Mengumpulkan semua komentar `ponytail:` di kode menjadi daftar utang teknis. |
| [`ponytail-gain`](skills/ponytail-gain/SKILL.md) | Menampilkan ringkasan penghematan kode dari penggunaan mode `ponytail`. |
| [`ponytail-help`](skills/ponytail-help/SKILL.md) | Referensi cepat perintah dan mode `ponytail`. |
| [`ponytail-review`](skills/ponytail-review/SKILL.md) | Meninjau perubahan kode khusus untuk mendeteksi bagian yang terlalu rumit. |

### Keamanan & Bot WhatsApp (2)

| Skill | Fungsi |
|---|---|
| [`threat-model`](skills/threat-model/SKILL.md) | Pemodelan ancaman keamanan desain aplikasi (STRIDE, PASTA, LINDDUN, risiko privasi) dengan laporan ke `threat-model/`. |
| [`whatsapp-bot-deep-audit`](skills/whatsapp-bot-deep-audit/SKILL.md) | Protokol audit dan pengujian fitur bot WhatsApp (Baileys) untuk pesan teks, balasan media, dokumen, view-once, dan fallback unduhan. |

---

## Kredit & Atribusi

Seluruh hak cipta tetap menjadi milik pembuat masing-masing:

- **Kelompok Remotion Video** (`remotion-*`): Resmi dari **Remotion** ([github.com/remotion-dev/skills](https://github.com/remotion-dev/skills)).
- **Kelompok Animasi & Design Engineering** (`animate`, `animate-expo`, `animation-vocabulary`, `ask-sonner`, `break-ui`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `mobile-native`, `pick-ui-library`, `prototype`, `review-animations`): Berdasarkan filosofi *design engineering* **Emil Kowalski** ([animations.dev](https://animations.dev/) / [sonner.emilkowal.ski](https://sonner.emilkowal.ski/)).
- **Kelompok Ponytail** (`ponytail`, `ponytail-audit`, `ponytail-debt`, `ponytail-gain`, `ponytail-help`, `ponytail-review`): **Ponytail Skill Suite** (Lisensi MIT).
- **`threat-model`**: **Grim Prompter** (*Threat Modeling Skill*).
- **`ui-ux-pro-max`**: Proyek komunitas **UI/UX Pro Max**.
- **`apple-design`, `design-dna`, `write-swift`**: Koleksi *skills* komunitas pengembang AI Agent.
- **`whatsapp-bot-deep-audit`**: Dibuat oleh **Lenz**.
