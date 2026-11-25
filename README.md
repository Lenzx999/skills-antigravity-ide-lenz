# Kumpulan Skills Antigravity IDE — Lenz

Koleksi **24 Agent Skills** pilihan untuk **Google Antigravity IDE** (dan kompatibel dengan format standar `SKILL.md` pada agen AI coding lainnya). Repositori ini menggabungkan berbagai *skills* yang digunakan dalam pengembangan UI/UX, animasi web & mobile, *design engineering*, penyederhanaan kode (*anti-over-engineering*), keamanan (*threat modeling*), hingga audit bot WhatsApp.

> **Website Resmi:** [https://lenznity.my.id](https://lenznity.my.id)

---

## Cara Memasang ke Antigravity IDE

Kamu bisa memasang *skills* ini secara otomatis menggunakan bantuan **Agent Antigravity** (cukup salin prompt di bawah) atau secara manual.

### Opsi 1: Cara Cepat (Prompt Siap Salin untuk Agent Antigravity)

Buka proyek kamu di **Antigravity IDE**, lalu salin dan kirim salah satu prompt berikut ke Agent:

**A. Pasang khusus untuk 1 proyek (Workspace Scope — `.agents/skills`):**
```text
Tolong clone atau download repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz (atau ambil dari folder lokal jika sudah ada), lalu salin semua folder skill di dalam direktori `skills/` ke folder `.agents/skills/` pada workspace proyek ini agar aktif di Antigravity IDE. Jangan hapus skill yang sudah ada sebelumnya, dan pastikan setiap folder berisi file `SKILL.md` beserta file pendukungnya secara utuh. Setelah selesai, verifikasi daftar skill yang berhasil terpasang.
```

**B. Pasang secara global untuk semua proyek (Global Scope — `~/.agents/skills`):**
```text
Tolong clone atau download repositori https://github.com/Lenzx999/skills-antigravity-ide-lenz, lalu salin seluruh folder skill di dalam direktori `skills/` ke folder global skills Antigravity (`~/.agents/skills/` di macOS/Linux atau `C:\Users\<USER>\.agents\skills\` di Windows). Jangan menimpa atau menghapus skill global lain yang sudah ada. Setelah selesai, laporkan daftar skill yang berhasil terpasang.
```

### Opsi 2: Cara Manual

1. Clone repositori ini:
   ```bash
   git clone https://github.com/Lenzx999/skills-antigravity-ide-lenz.git
   ```
2. Salin seluruh folder di dalam `skills/` ke salah satu lokasi berikut:
   - **Per Proyek (Workspace):** `<folder-proyek-kamu>/.agents/skills/`
   - **Global (Semua Proyek):**
     - Windows: `C:\Users\<Username>\.agents\skills\`
     - macOS / Linux: `~/.agents/skills/`
3. Restart atau buka sesi chat baru di **Antigravity IDE**, lalu sebutkan nama skill atau topiknya saat memberi perintah ke Agent.

---

## Daftar Skills & Fungsinya (24 Skills)

### 1. Animation & Design Engineering (12 Skills)
Kelompok skill ini fokus pada kualitas interaksi, *motion*, detail antarmuka, serta pengalaman pengguna yang halus di web maupun mobile.

| Nama Skill | Fungsi Utama |
|---|---|
| [`animate`](skills/animate/SKILL.md) | Merancang dan menulis kode animasi web dari nol secara terstruktur (menentukan apakah perlu animasi, tujuan, tool, properti, kurva/durasi, interupsi, dan transisi keluar). |
| [`animate-expo`](skills/animate-expo/SKILL.md) | Membangun animasi di React Native & Expo menggunakan Reanimated, Gesture Handler, Expo Router, dan `expo-haptics` agar tetap 60/120fps di UI thread perangkat nyata. |
| [`animation-vocabulary`](skills/animation-vocabulary/SKILL.md) | Kamus *reverse-lookup* untuk mengubah deskripsi awam efek animasi (misal: "efek memantul saat popover muncul") menjadi istilah teknis yang tepat. |
| [`ask-sonner`](skills/ask-sonner/SKILL.md) | Panduan instalasi, penggunaan, styling, theming, dark mode, dan troubleshooting library toast React **Sonner**. |
| [`break-ui`](skills/break-ui/SKILL.md) | Menguji ketahanan komponen UI dengan data *worst-case* (nama super panjang, email tanpa spasi, angka ekstrem, daftar kosong, teks non-Latin, emoji) di balik toggle demo. |
| [`emil-design-eng`](skills/emil-design-eng/SKILL.md) | Menerapkan prinsip *design engineering*, kehalusan komponen, keputusan animasi, dan detail UI yang terasa natural. |
| [`find-animation-opportunities`](skills/find-animation-opportunities/SKILL.md) | Audit *read-only* pada codebase/UI untuk menemukan bagian yang layak diberi animasi dan menolak bagian yang justru mengganggu jika dianimasikan. |
| [`improve-animations`](skills/improve-animations/SKILL.md) | Mensurvei kode animasi pada codebase (*read-only*) lalu menyusun roadmap perbaikan terprioritas untuk dieksekusi. |
| [`mobile-native`](skills/mobile-native/SKILL.md) | Kumpulan perbaikan CSS dan meta-tag agar web app terasa seperti aplikasi native di ponsel (mengatasi sticky hover, tap flash, bug `100vh`, auto-zoom input, notch, dll). |
| [`pick-ui-library`](skills/pick-ui-library/SKILL.md) | Membantu memilih library frontend yang tepat dari daftar terkurasi (dialog, toast, chart, command menu, drag-and-drop, virtualization, state, styling, dll). |
| [`prototype`](skills/prototype/SKILL.md) | Membangun beberapa versi UI yang benar-benar berbeda lengkap dengan *visual picker* agar bisa dibandingkan langsung sebelum dipilih. |
| [`review-animations`](skills/review-animations/SKILL.md) | Melakukan review kode animasi dan transisi dengan standar tinggi agar gerakan terasa cepat, responsif, dan tidak berlebihan. |

### 2. UI/UX, Design System & Swift (4 Skills)

| Nama Skill | Fungsi Utama |
|---|---|
| [`apple-design`](skills/apple-design/SKILL.md) | Menerjemahkan pendekatan desain antarmuka dan motion fisik ala Apple ke web (gesture, spring, momentum, material transparan, tipografi, `reduced-motion`). |
| [`design-dna`](skills/design-dna/SKILL.md) | Mengekstrak, mendefinisikan, dan menerapkan *Design DNA* dalam 3 dimensi: design system (token), gaya desain, dan efek visual (Canvas, WebGL, 3D, shader, scroll) dalam profil JSON terstruktur. |
| [`ui-ux-pro-max`](skills/ui-ux-pro-max/SKILL.md) | Mesin referensi UI/UX lokal (dilengkapi skrip pencarian Python & dataset) berisi 79 style, 192 palet warna, 74 pairing font, 119 panduan UX, 105 ikon, 17 preset GSAP, 25 tipe chart, dan 22 stack framework. |
| [`write-swift`](skills/write-swift/SKILL.md) | Panduan menulis kode Swift modern (Swift 6.x, value types, data-race safety, `@concurrent`, actors, generics `some` vs `any`, Swift Testing, dan optimasi memori). |

### 3. Anti-Over-Engineering — Ponytail Suite (6 Skills)
Kumpulan skill untuk mencegah kode berbelit-belit (*over-engineering*), mengutamakan kesederhanaan, YAGNI, dan fitur bawaan bahasa/platform.

| Nama Skill | Fungsi Utama |
|---|---|
| [`ponytail`](skills/ponytail/SKILL.md) | Mengarahkan agent memilih solusi paling sederhana, minimal, dan langsung bekerja (mendukung mode `lite`, `full`, dan `ultra`). |
| [`ponytail-audit`](skills/ponytail-audit/SKILL.md) | Audit seluruh repositori (*read-only*) untuk menemukan kode yang terlalu rumit, abstraksi berlebihan, atau dependensi yang bisa diganti fitur bawaan. |
| [`ponytail-debt`](skills/ponytail-debt/SKILL.md) | Mengumpulkan seluruh komentar `ponytail:` di dalam codebase menjadi daftar utang teknis (*debt ledger*). |
| [`ponytail-gain`](skills/ponytail-gain/SKILL.md) | Menampilkan ringkasan dampak terukur penggunaan mode `ponytail`. |
| [`ponytail-help`](skills/ponytail-help/SKILL.md) | Kartu referensi cepat untuk semua mode, perintah, dan skill dalam ekosistem `ponytail`. |
| [`ponytail-review`](skills/ponytail-review/SKILL.md) | Code review yang berfokus khusus mencari *over-engineering* (duplikasi standard library, dependensi tak perlu, abstraksi spekulatif). |

### 4. Security & Bot WhatsApp (2 Skills)

| Nama Skill | Fungsi Utama |
|---|---|
| [`threat-model`](skills/threat-model/SKILL.md) | Melakukan pemodelan ancaman keamanan (*threat modeling*) secara *read-only* menggunakan metodologi **Grim Prompter** (STRIDE, PASTA, LINDDUN, analisis privasi GDPR/CCPA) dan menghasilkan laporan di folder `threat-model/`. |
| [`whatsapp-bot-deep-audit`](skills/whatsapp-bot-deep-audit/SKILL.md) | Metodologi audit mendalam dan protokol pengujian multi-payload untuk fitur bot WhatsApp berbasis Baileys (teks langsung, reply gambar/video/dokumen, media view-once, dan fallback download stream). |

---

## Kredit & Atribusi Pembuat Asli

Repositori ini adalah **kompilasi / kurasi ulang** dari berbagai *skills* yang digunakan dalam alur kerja Antigravity IDE. Seluruh hak cipta, kredit, dan penghargaan tetap menjadi milik pembuat aslinya masing-masing:

- **Kelompok Animation & Design Engineering** (`animate`, `animate-expo`, `animation-vocabulary`, `ask-sonner`, `break-ui`, `emil-design-eng`, `find-animation-opportunities`, `improve-animations`, `mobile-native`, `pick-ui-library`, `prototype`, `review-animations`):
  Disusun berdasarkan filosofi *design engineering* dan animasi **Emil Kowalski** ([animations.dev](https://animations.dev/) / [sonner.emilkowal.ski](https://sonner.emilkowal.ski/)).
- **Kelompok Ponytail Suite** (`ponytail`, `ponytail-audit`, `ponytail-debt`, `ponytail-gain`, `ponytail-help`, `ponytail-review`):
  Karya **Ponytail Skill Suite** — dirilis di bawah **Lisensi MIT** (tercantum pada metadata skill `ponytail`).
- **Skill `threat-model`**:
  Bagian dari **Grim Prompter** (*Threat Modeling Skill*).
- **Skill `ui-ux-pro-max`**:
  Karya proyek komunitas **UI/UX Pro Max**.
- **Skill `apple-design`, `design-dna`, `write-swift`**:
  Koleksi *skills* komunitas pengembang Antigravity / AI Agent (tidak mencantumkan nama penulis spesifik di berkas sumbernya).
- **Skill `whatsapp-bot-deep-audit`**:
  Disusun oleh **Lenz** ([lenznity.my.id](https://lenznity.my.id)) untuk standar audit dan ketahanan media bot WhatsApp.

> Jika kamu adalah pemilik asli salah satu *skill* di atas dan ingin menambahkan tautan repositori sumber atau penyesuaian atribusi, silakan ajukan *issue* atau hubungi melalui [lenznity.my.id](https://lenznity.my.id).

---

## Kontak & Website

- **Website:** [https://lenznity.my.id](https://lenznity.my.id)
