# Changelog

## 2.0.0 — 2026-11-05

### Added

- Skill flow-filmmaking untuk mengarahkan produksi lengkap dan melanjutkan proyek.
- Kontrak catatan produksi per proyek, shot, aset dan attempt, dengan status unknown untuk pemulihan job ambigu.
- Integrasi instruksional OpenMontage sebagai dependensi lokal, dengan pilihan FFmpeg, Remotion dan HyperFrames, preview serta sumber edit.
- Workflow analisis video dan penilaian audio melalui Earshot dengan pemakaian cache/proses yang efisien.
- Penamaan proyek/aset tetap, pemetaan judul Flow per proyek dan pemakaian ulang asset references.

### Changed

- Look bersama dan keputusan shot disimpan sekali. Detail diteruskan ke prompt final, revisi hanya memperbarui bagian terkait.
- Generasi melalui MCP memakai job ID terarah, batas kredit per scene serta total, satu varian dan nol retry sebagai default eksplisit.
- Editing kini dapat dijalankan ketika diminta, dengan artefak yang dapat diedit manual.

### Compatibility and validation

- Tiga skill lama tetap tersedia. Proyek lama dimigrasi saat dipakai tanpa regenerasi footage.
- Tidak membundel kode, runtime atau kredensial OpenMontage. Memakai dependensi yang tersedia di mesin pengguna.
- Pemeriksaan struktur, referensi, routing dan skenario workflow dilakukan sebelum publikasi. Uji generasi berbayar, benchmark penggunaan harian dan render lengkap tiap runtime belum dilakukan.

## Sebelum 2.0.0

- Versi sebelumnya belum diberi nomor. Riwayat Git sampai 30 Oktober 2026 memuat tiga skill, standar cinematic dan cheat sheet visual.
