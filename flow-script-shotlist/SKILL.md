---
name: flow-script-shotlist
description: "Susun atau revisi naskah dan shot list video untuk produksi di Google Flow, termasuk beat cerita, dialog, blocking, kamera, kontinuitas dan kebutuhan aset. Gunakan untuk mengubah ide menjadi rencana klip Veo 3.1 atau Omni 1.1 Flash; bukan untuk menulis prompt video siap salin atau membuat gambar referensi."
---

# Naskah dan shot list untuk produksi Flow

Ubah ide menjadi cerita yang dapat difilmkan melalui klip generatif. Pisahkan naskah, keputusan per-shot, dan rencana penyambungan. Pengarahan harus mengikuti tujuan cerita serta pilihan gaya pengguna; jangan selalu memaksakan hook komedi, hand-held, telephoto, atau finale orbit.

## Konteks awal

Gunakan tujuan, audiens, durasi akhir, rasio, tone, bahasa, karakter dan aset yang sudah ditetapkan. Bila pengguna hanya memberi ide, buat asumsi rutin yang cukup untuk menghasilkan draft konkret dan sebutkan secara singkat. Jangan menunda draft untuk pilihan teknis yang belum memengaruhi cerita.

Jika paket aset tersedia, pakai ID dan varian yang sama. Bedakan aset tersedia dari yang perlu dibuat. Jika aset belum ada, catat kebutuhan minimal; jangan mengklaim sudah membuat gambar.

## Susun cerita yang terlihat dan terdengar

Tentukan perubahan utama: apa yang diketahui, diinginkan atau dilakukan karakter pada awal dan akhir. Bentuk beat yang relevan, lalu tulis aksi yang dapat diamati. Emosi diperlihatkan melalui perilaku, situasi, komposisi atau bunyi; jangan hanya menuliskan nama emosi.

Dialog harus sesuai waktu dan bahasa yang diminta. Pisahkan kata-kata dialog dari arahan performa. Sediakan jeda untuk aksi atau reaksi ketika diperlukan; jangan mengisi seluruh durasi dengan percakapan. Perkirakan pembacaan dengan tempo yang sesuai adegan dan nyatakan perkiraan jika belum diuji.

Naskah dapat sederhana atau kompleks sesuai permintaan. Panjang cerita tidak harus sama dengan panjang satu generasi. Untuk video produk atau observasional tanpa karakter, gunakan perubahan visual atau informasi sebagai struktur beat.

## Turunkan menjadi shot list

Tiap shot mencatat:

- ID shot dan fungsi dramatis/informasinya;
- perkiraan durasi edit, serta durasi klip generasi bila sudah diketahui;
- aset dan keadaan awal subjek/properti;
- aksi, blocking, arah pandang serta perkembangan;
- focal length numerik (mm, acuan full-frame), framing, camera angle, fokus dan gerakan kamera yang relevan;
- cahaya, suara/dialog dan keadaan akhir;
- kontinuitas serta sambungan ke shot berikut.

Framing, angle, lensa/look dan gerakan adalah keputusan terpisah. Pada workflow pengguna ini, selalu pilih focal length dan tulis hasil visualnya bersama ukuran shot serta angle, lalu tentukan posisi/jarak relatif kamera agar framing masuk akal. Lensa 85mm tidak otomatis berarti close-up; framing juga dipengaruhi jarak dan ukuran sensor. Gunakan acuan full-frame sebagai konvensi dokumen, bukan klaim ukuran sensor atau simulasi optik presisi dari model. Hubungkan gerak kamera dengan perubahan cerita. Shot statis, komposisi tengah, wide-angle dan pengulangan angle tetap sah bila tepat.

Pilih satu fungsi dominan per shot sebagai awal. Beberapa gerak kecil atau aksi bertahap diperbolehkan bila jelas dan cukup waktu. Hindari memecah satu aksi penting hanya karena membagi durasi secara merata.

## Rencanakan kontinuitas dan produksi

Tetapkan identitas/kostum, keadaan properti, hubungan ruang, arah cahaya pada set, arah gerak dan eyeline. Tunjukkan apa yang berubah pada akhir shot. Sudut kamera baru tidak otomatis mengubah posisi benda atau arah cahaya dunia.

Jika video akhir lebih panjang dari satu klip, rencanakan beberapa klip dan titik edit yang masuk akal. Durasi edit boleh lebih pendek dari hasil generasi; sisakan handle bila membantu. Jumlah shot dan jumlah generasi tidak selalu sama, tetapi jangan menjanjikan multi-shot presisi tanpa mempertimbangkan mode dan model.

Untuk keputusan yang bergantung pada fitur, lihat [tabel Flow terbaru](https://support.google.com/flow/answer/16352836?hl=en) atau bukti UI pengguna. Jangan menyalin durasi 27-30 detik dari contoh Seedance. Jika varian belum dipilih, rencana shot bisa tetap dibuat dengan durasi target dan catatan penyesuaian produksi.

## Keluaran dan serah-terima

Berikan ringkasan konsep singkat, naskah sesuai kebutuhan, shot list, dan daftar aset yang belum ada. Gunakan struktur secukupnya; satu-shot tidak memerlukan dokumen panjang.

Baca [format shot list dan contoh](references/shotlist-format.md) saat menyusun rencana multi-shot atau menyerahkannya ke tahap prompt video. ID shot dan aset harus tetap konsisten pada revisi; jelaskan perubahan hanya jika memengaruhi produksi.

Hasil siap diteruskan ke penyusun prompt video. Jangan memasukkan token API atau memaksakan sintaks prompt pada naskah. Jika pengguna sudah meminta alur lengkap, lanjutkan tahap berikut menggunakan hasil ini tanpa menjadikan serah-terima sebagai gerbang persetujuan baru.

## Pemeriksaan akhir

Periksa total durasi, kelayakan dialog, perubahan keadaan properti, posisi karakter, arah kamera serta sambungan. Temukan konflik seperti single take dengan cut, close-up yang harus sekaligus memperlihatkan semua ruang, atau aksi padat dalam klip pendek. Revisi rencananya sebelum meneruskan ke prompt.
