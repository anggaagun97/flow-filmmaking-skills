---
name: flow-reference-assets
description: "Rancang character sheet, prop sheet, location plate atau set reference untuk produksi video di Google Flow. Buat prompt gambar, spesifikasi kontinuitas, dan pemetaan aset untuk shot list atau prompt video. Gunakan saat pengguna menyiapkan atau memperbaiki referensi visual; bukan untuk menulis naskah lengkap atau prompt gerak video."
---

# Referensi karakter, properti dan set untuk Flow

Ubah brief dan referensi pengguna menjadi aset visual yang mudah dibaca, konsisten, serta memiliki fungsi jelas pada produksi. Default hasil kerja adalah rancangan dan prompt gambar siap pakai. Nyatakan apakah gambar sudah tersedia atau baru direncanakan; jangan menyebut rancangan sebagai gambar yang sudah dibuat.

## Mulai dari kebutuhan shot

Gunakan konteks proyek yang sudah ada: karakter, kostum, benda, tempat, gaya, rasio, dan shot yang akan dibuat. Jika belum ada shot list, siapkan referensi minimum yang sesuai cerita tanpa mengarang kebutuhan detail yang tidak relevan. Buat asumsi rutin secara singkat; tanyakan hanya informasi yang mengubah identitas atau arah visual secara berarti.

Periksa gambar yang tersedia sebelum mengusulkan perubahan. Catat benturan wajah, kostum, skala properti, keadaan benda, atau arah cahaya. Pertahankan ciri yang secara eksplisit diminta pengguna.

## Pilih jenis aset dan penataannya

- **Karakter:** untuk workflow pengguna ini, gunakan tepat tiga panel dalam satu character sheet: (1) close-up dengan wajah tajam dan jelas; (2) full shot menghadap depan, seluruh tubuh dari kepala hingga kaki terlihat, area wajah diburamkan; (3) full shot menghadap belakang, seluruh tubuh terlihat. Semua wajah yang terlihat pada panel full shot harus diburamkan; pada tampak belakang murni wajah memang tidak terlihat, jangan menambahkan wajah ke belakang kepala. Pertahankan rambut, proporsi tubuh, kostum dan aksesori yang sama pada ketiga panel. Blur hanya area wajah, bukan pakaian atau seluruh kepala. Gunakan latar netral dan cahaya merata agar detail kostum terbaca. Simpan versi kostum berbeda sebagai varian yang jelas. Ini preferensi pengguna, bukan syarat universal model; ubah hanya bila pengguna meminta format lain.
- **Properti:** bentuk, ukuran relatif, bahan, warna, detail khas serta keadaan yang diperlukan. Tambahkan tampak lain atau keadaan terbuka/tertutup hanya jika membantu shot. Satu desain harus tetap satu desain di semua tampak.
- **Set/lokasi:** tata ruang dan hubungan antarobjek, furnitur, horizon, jalur gerak, sumber cahaya dan kondisi lingkungan. Location plate kosong berguna jika karakter akan ditambahkan kemudian; karakter tidak wajib dihilangkan jika komposisi adegan memang membutuhkan mereka.
- **Frame adegan:** satu komposisi final untuk dianimasikan. Pisahkan dari sheet atau collage referensi. Tentukan posisi karakter, properti dan framing berdasarkan kebutuhan shot.

Gunakan prompt gambar yang menjelaskan keluaran visual, pembagian tampak jika ada, detail yang tetap, serta pengecualian yang relevan. Hindari mengunci seluruh aset pada film grain atau cahaya dramatis bila akan menyulitkan pemakaian lintas shot. Sebut bahwa latar studio pada sheet tidak dimaksudkan sebagai lokasi film ketika perlu.

## Look adegan dan kontinuitas cahaya

Untuk frame adegan produksi, tentukan focal length numerik acuan full-frame, framing, angle dan posisi/jarak relatif; aperture look, target fokus, bokeh/DoF; referensi film stock dan interpretasi warna/kontras; sumber, arah dan kualitas cahaya yang membentuk subjek; serta atmosfer dan dampaknya pada karakter/material/visibilitas. Gerak kamera yang direncanakan membutuhkan ruang dan lapisan foreground–midground–background yang mendukungnya. Gunakan keputusan adegan yang sudah ada; bila metadata tidak diketahui, nyatakan sebagai look.

Character/prop identity sheet tetap netral, jelas dan mudah digunakan lintas shot; jangan memaksakan lighting dramatis, blur DoF atau grain pada sheet yang menghilangkan detail identitas. Pemburaman wajah full shot tetap hanya aturan panel sheet. Simpan look produksi pada frame adegan atau spesifikasi set, agar tidak mencampur identitas dengan treatment adegan.

Catat posisi sumber cahaya dalam koordinat ruang, sifat permukaan, keadaan basah/kering, arah angin dan perubahan properti yang perlu diwariskan. Sudut baru tidak memindahkan jendela atau menukar tangan pemegang benda. Film stock adalah rujukan karakter gambar, bukan jaminan emulasi tepat.

## Petakan fungsi aset ke Flow

Ingredients/references mengarahkan identitas atau ciri aset; frame awal/akhir menetapkan kondisi visual pada batas klip. Jangan memasukkan seluruh character sheet sebagai frame awal kecuali video memang harus dimulai dari sheet tersebut.

Blur wajah pada panel full shot hanya untuk sheet referensi. Wajah karakter pada gambar adegan dan video tetap jelas, kecuali pengguna meminta sebaliknya. Panel close-up menjadi acuan identitas wajah; panel full shot menjadi acuan tubuh dan pakaian. Untuk properti dengan beberapa tampak, pilih satu tampak produksi bila sheet menyebabkan model menggandakan benda.

Jangan menebak jumlah slot referensi atau dukungan varian model. Jika mode yang tersedia tidak menerima referensi terpisah, rancang satu frame adegan yang bersih untuk mode Frames. Menyebut aset di teks tidak menggantikan pemasangan gambar pada antarmuka.

Gunakan ID internal sederhana yang konsisten, misalnya CH-01, PR-01 dan SET-01. ID itu untuk dokumen proyek, bukan ID native Flow atau token upload. Nama file dan status harus mencerminkan aset yang benar-benar ada.

## Keluaran

Untuk satu aset, cukup beri spesifikasi singkat, prompt gambar siap salin, ciri yang harus konsisten, dan fungsi pemakaiannya di Flow. Untuk satu paket, tambahkan daftar aset dengan ID, varian, sumber/file jika tersedia, serta status planned, available atau needs-revision.

Baca [format paket dan contoh](references/asset-package.md) jika menyiapkan beberapa aset atau menyerahkannya ke tahap naskah/prompt video. Gunakan tabel Markdown sebagai default; buat JSON hanya bila berguna untuk pengguna atau integrasi.

Jika pengguna meminta gambar benar-benar dibuat, gunakan alur pembuatan gambar yang mereka pilih. Preferensi proyek ini adalah Flow; jangan diam-diam berpindah provider. Tugas menyusun prompt tidak dengan sendirinya memerlukan generasi gambar atau kredit.

Koreksi aturan atau format sheet tidak otomatis berarti menjalankan generasi ulang. Simpan prompt revisi dan tandai gambar lama needs-revision. Sebelum mengulang job yang timeout atau dilaporkan gagal, periksa antrean dan aset Flow; unduh hasil yang sudah ada tanpa regenerasi. Gunakan satu hasil per aset dan tanpa retry otomatis kecuali pengguna meminta batch atau iterasi. Jangan menggunakan generasi berbayar berulang untuk menguji perbaikan MCP; setelah satu kegagalan integrasi, hentikan submit dan lakukan diagnosis tanpa generasi sampai status job sebelumnya jelas.

## Pemeriksaan akhir

- Apakah tiap tampak menunjukkan orang/benda yang sama, dengan kostum dan detail yang sesuai varian?
- Apakah sheet karakter memiliki tiga panel: wajah close-up tajam, full shot depan dengan wajah blur, dan full shot belakang tanpa wajah terlihat (atau wajah blur jika sebagian terlihat)?
- Apakah referensi memberikan informasi yang dibutuhkan shot, tanpa terlalu banyak bagian yang bersaing?
- Apakah lokasi menyediakan ruang untuk aksi serta pencahayaan yang konsisten?
- Apakah gambar diposisikan sebagai ingredient atau frame dengan benar?
- Apakah aset baru dirancang dibedakan dari aset yang tersedia?

Landasan: inspeksi gambar dan metode TRY CGI, disesuaikan dengan [cara menambahkan referensi/frame di Flow](https://support.google.com/flow/answer/16353334?co=GENIE.Platform%3DDesktop&hl=en). Pilihan gaya sumber tidak menjadi batas universal pengguna.
