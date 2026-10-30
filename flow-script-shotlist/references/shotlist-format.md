# Format shot list dan contoh

Tabel Markdown cukup untuk sebagian besar proyek. Jangan memaksa pengguna mengisi formulir ini sebelum Anda membuat draft.

| Shot | Durasi edit / klip | Fungsi | Aset dan awal | Aksi | Kamera | Audio | Akhir dan sambungan |
|---|---|---|---|---|---|---|---|
| S01 | 4s / rencana 4s | Memperkenalkan amplop | CH-01 duduk, PR-01 tertutup | Pria mulai membuka amplop | Medium, eye-level, kamera stabil | Kertas, angin | Amplop terbuka; sambungkan gerak tangan |
| S02 | 4s / rencana 4s | Menemukan kekosongan | PR-01 terbuka | Ia memeriksa bagian dalam dan berhenti | Insert tangan dan amplop | Kertas mereda | Tangan berhenti; cut ke reaksi |
| S03 | 4s / rencana 4s | Memperlihatkan kesadaran | CH-01 masih memegang amplop | Ia menatap orang di seberang, di luar frame | Close-up, push-in ringan | Angin | Tahan ekspresi penutup |

Ini contoh cerita 12 detik dengan satu shot per klip, tanpa dialog. Rencana durasi perlu sesuai opsi aktual Flow. Referensi contoh belum otomatis tersedia dan jumlahnya tidak menyatakan batas slot model.

## Lengkapi keputusan visual contoh

Asumsi contoh: exterior sore, stock/look proyek Kodak VISION3 250D-inspired, kulit natural, grain halus dan highlight terkontrol. Matahari rendah dari barat menjadi back-side key, bounce langit memberi fill wajah. Udara kering jernih dengan angin ringan menggerakkan flap amplop; tidak ada debu padat yang tidak diminta.

| Shot | Kamera dan optik | Fokus | Lighting dan atmosfer |
|---|---|---|---|
| S01 | 50mm full-frame, medium waist-up, eye level, static | f/4 look, wajah dan amplop terbaca, bokeh lembut | Soft bounce pada wajah, tepi hangat matahari; angin pelan |
| S02 | 100mm macro look, insert tangan/amplop, slight high angle, static | f/8 look, isi amplop menjadi target, DoF tipis pada jarak dekat | Arah matahari sama, kertas memantulkan cahaya; tangan kanan mempertahankan pegangan |
| S03 | 85mm full-frame, close-up, eye level, slow physical push-in | f/2.8 look, mata dekat tajam, latar lembut | Fill wajah tetap terbaca, back-side edge konsisten; angin tetap dari arah yang sama |

Rentang framing bergantung posisi/jarak. Ini keputusan kreatif untuk contoh, bukan hasil generasi atau metadata kamera asli. Semua shot mewarisi stock/look dan arah sumber dunia yang sama; posisi sumber relatif terhadap kamera dapat berubah.

## Catatan yang tidak muat di tabel

- **Kontinuitas:** CH-01 mengenakan varian kostum yang sama; PR-01 tidak kembali tertutup setelah S01. Posisi sumber cahaya tetap pada set.
- **Blocking:** orang yang ditatap tetap berada pada sisi yang konsisten; bukan karakter baru yang tiba-tiba muncul.
- **Aset kurang:** karakter, lokasi, amplop dan frame awal per-shot bila mode Frames dipilih.
- **Edit:** sambungan tangan dari S01 ke S02 perlu diperiksa; aksi tidak harus benar-benar match jika hasil generasi berbeda. Dapat memilih cut pada jeda yang lebih aman.

## Bentuk serah-terima per shot

Gunakan nama berikut bila perlu format terstruktur: shot_id, story_function, target_edit_duration_s, generation_duration_s, asset_ids, initial_state, action, camera (focal_length_mm, framing, angle, relative_position, movement, aperture_look, focus_target, depth_of_field, bokeh), film_stock_look, lighting (source, world_direction, quality, shaping), atmosphere_and_effects, audio_dialogue, continuity, final_state, transition.

Isi yang belum diketahui ditandai sebagai asumsi atau belum ditentukan. Jangan membuat path gambar, ID upload Flow, pilihan model, atau status render palsu. Tahap prompt video boleh mengubah cara penulisan tanpa mengubah cerita, dialog dan kontinuitas yang sudah dipilih pengguna.

## Landasan

- [TRY CGI: pengarahan kamera](https://materials.trycgi.xyz/p/move-camera-prompts)
- [TRY CGI: pipeline dan kontinuitas](https://materials.trycgi.xyz/p/secret-prompts-how-we-made-it)
- [Google: pengarahan Veo 3.1](https://cloud.google.com/blog/products/ai-machine-learning/ultimate-prompting-guide-for-veo-3-1)
- [Google Flow: fitur model](https://support.google.com/flow/answer/16352836?hl=en)

Ini sintesis materi publik yang diperiksa pada 28 Oktober 2026, bukan salinan prompt terkunci atau bukti uji generasi.
