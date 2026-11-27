---
name: remotion-tiktok-viral
description: Standar produksi video Remotion vertikal (TikTok/Reels/Shorts) dan horizontal yang tajam bebas blur, bebas AI slop, beritme cepat, dengan audio auto-ducking dan kepatuhan moderasi TikTok.
---

# Remotion TikTok & Viral Production Standard

Gunakan skill ini bersama `remotion-best-practices` dan `antislop` / `antislop-ui` setiap kali membuat video Remotion agar hasil langsung siap tayang di media sosial tanpa revisi berulang.

## 1. Ukuran, Safe Area & Anti-Blur
- **Vertikal (TikTok/Reels/Shorts)**: `1080 x 1920` @ `30 fps`, durasi ideal `25–45 detik`.
- **Safe Area TikTok**:
  - Konten utama: `top >= 140px`, `bottom >= 500px`, `left >= 48px`, `right >= 92px` (bebas HUD kanan & caption bawah TikTok).
  - Subtitle: `bottom: 390px`, teks `34–38px` tebal, 3–4 kata per baris di atas blok solid `#000000`.
- **Horizontal (YouTube/Web)**: `1920 x 1080` @ `30 fps`.
- **Anti-Blur (`remotion.config.ts`)**:
  - Wajib `Config.setVideoImageFormat("png")`, `Config.setCrf(6)` (atau maksimal `12`), dan `Config.setX264Preset("slow")`.
  - Dilarang memperbesar gambar/screenshot melebihi `110%` ukuran aslinya atau menggeser/pan terus-menerus pada teks UI kecil.

## 2. Anti-Slop & Retensi Penonton
- Gunakan warna murni kontras tinggi (`#000000` / `#FFFFFF` / surface solid) dengan 1 warna aksen fokus. Hindari orb buram, background grid generik, dan efek glass berlebihan.
- **Aturan 3-Detik Pertama**: Pembuka langsung mengangkat masalah atau hasil nyata dengan gerak cepat.
- **Pacing 1,5–2 Detik**: Pastikan ada perubahan fokus, pergantian adegan gelap/terang, atau aksi UI setiap 1,5–2 detik.
- Gunakan **1 fokus pesan + maksimal 2–3 elemen** per layar dengan judul `56–80px` dan teks isi minimal `24px`.

## 3. Lapisan Audio & Kepatuhan TikTok
- **Voiceover**: Gunakan narasi alami (misal Google AI Studio TTS `gemini-2.5-flash-preview-tts` atau rekaman asli), dinormalisasi ke `-15 LUFS` via `ffmpeg`.
- **Auto-Ducking BGM + SFX**: Turunkan volume musik latar saat suara bicara aktif; pasang SFX (`whoosh`, `switch`, `pop-soft`, `mouse-click`, `pen-scribble`, `shutter-modern`) tepat pada frame aksi.
- **Keamanan Moderasi TikTok**:
  - Jangan menampilkan URL mentah/domain website berulang di layar maupun caption.
  - Hindari kata kunci pemicu filter (*hack*, *bot*, *gratis* + ajakan klik link).
  - Jika memakai suara/visual sintesis AI, aktifkan toggle **"Konten dibuat dengan AI"** saat mengunggah.
