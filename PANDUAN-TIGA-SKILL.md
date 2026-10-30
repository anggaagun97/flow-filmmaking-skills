# Tiga skill produksi untuk Google Flow

Disusun dari metode terpadu TRY CGI dan riset Google Flow pada 28 Oktober 2026. Target video: Veo 3.1 dan Gemini Omni Flash 1.1. Ketiga skill menyiapkan materi dan prompt; tidak otomatis menjalankan generasi atau memakai kredit.

| Skill | Dipakai untuk | Hasil utama |
|---|---|---|
| `$flow-reference-assets` | Menyiapkan karakter, properti dan set | Spesifikasi aset, prompt gambar, kontinuitas, pemetaan referensi |
| `$flow-script-shotlist` | Mengembangkan ide menjadi cerita yang dapat diproduksi | Naskah, beat, shot list, blocking, kamera, suara dan sambungan |
| `$flow-video-prompts` | Menerjemahkan brief/shot list ke model dan mode Flow | Setup Flow, penempatan aset, prompt siap salin dan pengecualian |

## Cara memakai

```text
Gunakan $flow-reference-assets untuk membuat rancangan character
sheet dua tokoh, prop sheet amplop, dan set dua kursi di bukit pasir.
```

```text
Gunakan $flow-script-shotlist untuk menulis cerita 24 detik tentang
dua tokoh tersebut: satu membuka amplop dan menemukan isinya kosong.
Tanpa dialog. Buat shot list dengan kontinuitas properti yang jelas.
```

```text
Gunakan $flow-video-prompts untuk menerjemahkan shot list tersebut
menjadi prompt Omni 1.1 Flash di Google Flow. Saya memakai mode
Frames dan sudah mempunyai frame awal untuk setiap shot.
```

Jika sudah ada naskah atau aset, langsung gunakan skill yang diperlukan. Tidak wajib mengulang semua tahap. Jika memulai dari ide, naskah kasar dapat menentukan kebutuhan aset, lalu shot list diperinci setelah referensi siap. ID karakter, properti dan shot dipertahankan antartahap.

## Ruang lingkup tiap skill

Skill aset tidak otomatis menulis naskah lengkap. Skill naskah tidak otomatis menghasilkan prompt video siap salin. Skill prompt mempertahankan cerita yang telah dipilih, lalu menyesuaikan cara penulisan dengan Veo, Omni, mode input dan pengecualian yang diminta.

Setiap skill dapat digunakan sendiri. Jika pengguna meminta alur lengkap, hasil satu tahap diteruskan ke tahap berikutnya tanpa gerbang persetujuan tambahan untuk pekerjaan yang sudah diminta.

## Negative prompt

Daftar pengecualian tetap dicatat. Bila field negative terpisah tersedia dan didukung, gunakan daftar unsur. Bila masuk prompt utama, tulis larangan yang jelas. Jangan menganggap tulisan “Negative prompt” otomatis menciptakan parameter. Contoh camera shake harus diperiksa agar tidak bertentangan dengan permintaan hand-held natural.

## Preferensi character sheet dan eksekusi

Character sheet pengguna ini memiliki tepat tiga panel: close-up dengan wajah jelas, full shot depan dengan wajah blur, dan full shot belakang. Semua bagian wajah yang terlihat pada full shot diburamkan; tampak belakang murni tidak menampilkan wajah. Tubuh, rambut dan pakaian tetap tajam. Wajah pada adegan/video tetap jelas, mengambil identitas dari panel close-up.

Gunakan satu hasil per aset/shot, tanpa retry otomatis sebagai awal. Bila MCP gagal atau status submit tidak jelas, periksa job, aset yang sudah jadi dan perubahan saldo sebelum mengulang. Diagnosis integrasi tidak menjadi rangkaian generasi berbayar. Semua percobaan masuk perhitungan biaya. Penggabungan klip dikerjakan manual oleh pengguna.

Setiap shot list dan prompt video pengguna ini mencantumkan focal length numerik (mm, acuan full-frame), ukuran shot, camera angle dan gerak kamera. Lengkapi dengan jarak/posisi relatif yang menghasilkan framing tersebut. Angka lensa bukan pengganti framing atau angle; pada frame-to-video pertahankan viewpoint/crop gambar awal dan jangan mengklaim model menjalankan simulasi optik presisi.

## Standar cinematic 30 Oktober 2026

Setiap prompt video wajib menjelaskan: gerak/static camera; focal length numerik full-frame, framing, angle dan jarak relatif; aperture look, target fokus, bokeh dan DoF; referensi film stock dengan karakter warna/kontras/grain/highlight; sumber/arah/kualitas lighting serta pembentukan subjek; atmosfer dan dampaknya pada karakter/material/adegan. Pilih sesuai cerita, pertahankan kontinuitas, dan jangan menganggap angka prompt sebagai metadata kamera atau kontrol model yang pasti.

Shot list menetapkan keputusan tersebut sebelum serah-terima. Frame adegan mengikuti look produksi; identity sheet tetap netral dan mempertahankan tiga panel yang sudah disepakati. Untuk input frame atau edit sempit, hormati keputusan visual yang tidak diminta berubah. Kode ringkas hanya digunakan bila diminta, dengan makna deskriptif yang jelas.

[Cheat sheet HTML offline](flow-video-prompts/assets/cinematic-cheat-sheet.html) menyediakan 58 foto ImageGen dengan satu karakter acuan, 12 GIF gerak kamera dari Google Flow (Omni Flash 1.1, 4 detik), dan fragmen prompt. HTML memakai foto tertaut; unduh bersama folder cinematic-imagegen-assets yang berada di sampingnya. [Referensi pengarahan](flow-video-prompts/references/cinematic-direction.md) menjelaskan penerapan dan batas bukti. Revisi ini belum diuji lewat generasi video.

## Status validasi

Struktur setiap skill diperiksa memakai validator skill-creator; metadata antarmuka dan tautan referensi lokal juga diperiksa. Sampel Amplop Kosong sudah dijalankan melalui Flow; pengulangan berlebihan dan cacat kontinuitas pada percobaan tersebut menjadi dasar perbaikan aturan eksekusi. Format character sheet tiga panel dengan wajah blur pada full shot telah diperbarui sesuai koreksi pengguna, tetapi belum digenerasikan atau diuji pada sampel baru. Data fitur dalam referensi diberi tanggal dan harus diperiksa ulang saat keputusan bergantung pada fitur terkini.

## Sumber proyek

Laporan riset dan gambar tetap tersimpan pada folder `trycgi-offline` di samping paket ini. Ketiga skill menyertakan referensi ringkas yang mandiri dan tautan sumber publik, sehingga tidak bergantung pada lokasi arsip di komputer ini. Tidak ada prompt berbayar tersembunyi yang diambil.
