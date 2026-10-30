# Pengarahan cinematic untuk workflow pengguna

## Isi wajib per prompt video

Standar pengguna, ditetapkan 30 Oktober 2026: setiap prompt generasi video harus membawa keputusan visual berikut, dipilih berdasarkan kebutuhan adegan. Ini konvensi workflow, bukan sintaks atau parameter resmi Google Flow.

| Unsur | Keputusan yang harus terbaca |
|---|---|
| Kamera | Gerak, arah dan sasaran; tulis locked-off/static bila diam. Untuk gerak bertahap, urutkan waktunya. |
| Optik dan komposisi | Focal length numerik dalam mm dengan acuan full-frame, ukuran shot, angle, posisi/jarak relatif yang memungkinkan framing. |
| Aperture dan fokus | f-number, target/plane fokus, tingkat depth of field, karakter bokeh dan apakah fokus tetap atau berpindah. Jika tidak ada blur/bokeh yang terlihat, nyatakan deep focus tanpa bokeh menonjol. |
| Karakter gambar | Referensi film stock bernama dan interpretasi warna, kontras, grain serta highlight yang sesuai adegan. Pertahankan stock dan arah grade antar-shot kecuali perubahan dimotivasi. |
| Lighting | Sumber termotivasi, arah, ukuran/kualitas cahaya, key/fill/negative fill atau rim yang relevan, dan dampaknya ke bentuk wajah/tubuh. |
| Atmosfer | Kondisi udara/cuaca dan intensitasnya, arah gerak, pengaruh terhadap cahaya, karakter, material dan visibilitas. Udara bersih tanpa efek tambahan tetap pilihan yang sah. |

Teks harus membuat hasil yang diinginkan terlihat, bukan hanya menumpuk angka dan nama. Angka lensa/aperture dan stock adalah arahan visual kecuali kontrol aktual tersedia. Jangan menjanjikan simulasi optik, exposure atau warna presisi. Cinematic bukan kewajiban gelap, bokeh kuat, film grain berat, atau kamera terus bergerak.

Untuk frame-to-video, pertahankan crop, viewpoint, fokus dan cahaya awal dari gambar. Beri angka sebagai lens/aperture look bila metadata tidak diketahui; jangan mengklaim mengetahui setelan asli. Nyatakan look stock yang selaras tanpa memaksa relighting/regrading yang tidak diminta. Bila keputusan wajib akan menentang frame, perbaiki rancangan frame terlebih dahulu atau jelaskan pertentangannya. Untuk edit sempit pada klip, pertahankan keputusan visual yang tidak diubah sebagai konteks; jangan merombak seluruh prompt atau mengarang metadata klip demi mengisi template.

## Pilihan ringkas berdasarkan fungsi

- **Ruang dan parallax:** 20–35mm untuk framing lingkungan sebagai titik awal; foreground, midground, background dan physical dolly/truck yang terbaca. Kamera dan jarak menentukan perspektif; lensa saja tidak menentukan framing.
- **Dialog dan potret:** 50–85mm sebagai titik awal, eye level, f/2.8–5.6 sesuai blocking. Letakkan fokus pada mata yang dibutuhkan; wajah tidak wajib kehilangan ketajaman demi bokeh.
- **Detail produk:** sekitar 90–105mm macro look bila close-focus diperlukan; f/5.6–8 masih dapat menghasilkan DoF tipis pada jarak dekat. Tentukan detail hero, tangan yang memegang, bahan serta pantulan sumber cahaya.
- **Fokus berlapis:** 24–35mm, f/8–11 sebagai arah awal, dengan jarak fokus yang memungkinkan beberapa plane terbaca. Rack focus adalah perubahan perhatian: nyatakan objek awal, objek akhir dan durasinya.
- **Film stock:** VISION3 50D/250D sebagai rujukan daylight; 200T/500T untuk tungsten/mixed-light dengan white balance yang sesuai. Portra/Gold/Velvia/Provia/HP5 adalah rujukan still-film bila dipilih; jangan menyebutnya stock sinema. Double-X memberi rujukan motion-picture hitam-putih. Jelaskan interpretasi tampilan, jangan menganggap nama stock menentukan satu grade mutlak.
- **Bentuk cahaya:** window key lembut dari samping dengan negative fill untuk gradasi pipi; Rembrandt untuk segitiga terang di pipi jauh; split untuk separuh wajah; butterfly untuk key depan-atas; rim untuk pemisahan. Pilih pola yang cocok dengan bentuk wajah dan blocking, bukan semua sekaligus. High-key tetap dapat memiliki dimensi; silhouette boleh menyembunyikan detail wajah bila memang dimaksudkan.
- **Atmosfer realistis:** haze mengurangi kontras jauh dan menampakkan berkas dengan sumber cahaya yang tepat; hujan memberi wet hair/fabric dan refleksi permukaan; angin mengarahkan rambut/kain/partikel bersama; debu terlihat terutama pada sorot; asap dan bara mengikuti sumber serta aliran udara; steam berasal dari sumber panas. Jangan menambahkan seluruh efek pada setiap adegan.

## Narasi, properti, performa dan suara

Untuk multi-shot atau iklan, mulai dari perubahan informasi/cerita, lalu buat blok aksi berurutan berisi framing, aksi, dialog/reaksi dan suara. Gunakan waktu sesuai durasi yang didukung, bukan menyalin contoh 30 detik sebagai satu generasi. Setup, upaya, konsekuensi, eskalasi dan callback dapat membantu komedi, tetapi bukan struktur wajib genre lain.

Catat identitas/kostum dan posisi karakter; tata ruang, jalur keluar-masuk serta eyeline; desain, tangan pemegang, orientasi dan keadaan hero prop. Keadaan akhir shot menjadi keadaan awal berikut. Arah sumber cahaya dunia tetap meskipun posisi kamera berubah. Arahan performa menjelaskan gesture, jeda, tempo dan reaksi. Pisahkan dialog, ambience, efek dan musik; tambahkan hanya yang diperlukan atau diminta. Continuity lock tidak menjamin hasil; periksa output sebelum mengklaim cocok.

## Kode ringkas hanya ketika diminta

Format default adalah bahasa alami yang eksplisit. Label slash/no-slash hanya shorthand deskriptif dan tidak selalu efektif. Jangan menganggap `/orbit`, `/macro`, `/luxury`, atau susunan token sebagai parser resmi, preset pasti, atau jaminan fisika. Jika diminta memakai kode, jelaskan ekspansi maksudnya, pertahankan keputusan visual wajib dan hindari konflik. Untuk prompt yang harus singkat, padatkan kalimat tanpa membuang unsur yang telah ditentukan pengguna. Sintaks fitur native seperti referensi karakter harus diverifikasi terhadap UI/dokumentasi aktual secara terpisah.

## Contoh baru: satu shot

```text
Slow physical dolly-in at seated eye level; 65mm full-frame-equivalent
lens, medium close-up from chest up, camera far enough to preserve
natural facial proportions. f/2.8 aperture look, focus held on the near
eye, shallow depth with a readable face and soft restrained bokeh.
Kodak VISION3 500T-inspired mixed-light negative: natural skin,
subtle grain and controlled practical highlights.
A large soft window key from camera-left shapes the cheek; negative
fill on camera-right preserves contour. A warm work lamp provides
a restrained rear edge. Rain outside beads on the glass; cool damp
ambience indoors, no rain falling inside. The mechanic lifts her gaze
from the workbench, pauses and exhales naturally. Preserve identity,
wardrobe, tool positions and lighting direction. One continuous take.
Sound: distant rain and a single quiet tool contact; no music or captions.
```

Contoh ini sintesis pengarahan, belum diuji lewat generasi. Untuk video tanpa manusia, terapkan pembentukan cahaya dan fokus pada subjek/bahan yang relevan.

## Rujukan dan status bukti

- Standar wajib di atas berasal dari instruksi pengguna; cheat sheet visual pendamping tersedia di `assets/cinematic-cheat-sheet.html` dan berisi ilustrasi, bukan emulasi stock terkalibrasi. Buka bila pengguna meminta melihat/membandingkan variabel; tidak perlu memuat seluruh HTML untuk setiap prompt.
- [Nikon: focal length](https://www.nikonusa.com/learn-and-explore/c/products-and-innovation/understanding-focal-length) dan [aperture](https://www.nikonusa.com/learn-and-explore/c/tips-and-techniques/understanding-maximum-aperture): dasar optik, bukan bukti presisi model generatif.
- [Kodak VISION3 250D](https://www.kodak.com/content/pdfs/KODAK-VISION3-250D-5207-7207-brochure.pdf) dan [Fujifilm data guide](https://asset.fujifilm.com/www/us/files/2020-04/9cdee030ab7fc76bbcfddbcd38650038/ProfessionalFilmDataGuide.pdf): referensi emulsi.
- [Artikel 99 kode](https://aimarketingit.com/99-slash-commands-for-google-flows-video-agent/) dan [Instagram carousel + caption](https://www.instagram.com/p/DewCrk_E23p/): dibaca lengkap pada riset 30 Oktober 2026. Materi shorthand bukan bukti dukungan resmi atau hasil deterministik.
- PromptWise /14, /15, /17, /18, /24, /25, /29, /32, /38, /39: ringkasan dipulihkan dari chat lama; teks primer belum diverifikasi ulang. Gunakan sintesis yang konsisten dengan standar pengguna, jangan mengklaim kutipan/katalog lengkap sudah terverifikasi. Google Share yang belum terbaca tidak digunakan sebagai dasar aturan.
