# Format shot list dan contoh

Tabel Markdown cukup untuk sebagian besar proyek. Jangan memaksa pengguna mengisi formulir ini sebelum Anda membuat draft.

| Shot | Durasi edit / klip | Fungsi | Aset dan awal | Aksi | Kamera | Audio | Akhir dan sambungan |
|---|---|---|---|---|---|---|---|
| S01 | 4s / rencana 4s | Memperkenalkan amplop | CH-01 duduk, PR-01 tertutup | Pria mulai membuka amplop | Medium, eye-level, kamera stabil | Kertas, angin | Amplop terbuka; sambungkan gerak tangan |
| S02 | 4s / rencana 4s | Menemukan kekosongan | PR-01 terbuka | Ia memeriksa bagian dalam dan berhenti | Insert tangan dan amplop | Kertas mereda | Tangan berhenti; cut ke reaksi |
| S03 | 4s / rencana 4s | Memperlihatkan kesadaran | CH-01 masih memegang amplop | Ia menatap orang di seberang, di luar frame | Close-up, push-in ringan | Angin | Tahan ekspresi penutup |

Ini contoh cerita 12 detik dengan satu shot per klip, tanpa dialog. Rencana durasi perlu sesuai opsi aktual Flow. Referensi contoh belum otomatis tersedia dan jumlahnya tidak menyatakan batas slot model.

## Catatan yang tidak muat di tabel

- **Kontinuitas:** CH-01 mengenakan varian kostum yang sama; PR-01 tidak kembali tertutup setelah S01. Posisi sumber cahaya tetap pada set.
- **Blocking:** orang yang ditatap tetap berada pada sisi yang konsisten; bukan karakter baru yang tiba-tiba muncul.
- **Aset kurang:** karakter, lokasi, amplop dan frame awal per-shot bila mode Frames dipilih.
- **Edit:** sambungan tangan dari S01 ke S02 perlu diperiksa; aksi tidak harus benar-benar match jika hasil generasi berbeda. Dapat memilih cut pada jeda yang lebih aman.

## Bentuk serah-terima per shot

Gunakan nama berikut bila perlu format terstruktur: shot_id, story_function, target_edit_duration_s, generation_duration_s, asset_ids, initial_state, action, camera, lighting, audio_dialogue, continuity, final_state, transition.

Isi yang belum diketahui ditandai sebagai asumsi atau belum ditentukan. Jangan membuat path gambar, ID upload Flow, pilihan model, atau status render palsu. Tahap prompt video boleh mengubah cara penulisan tanpa mengubah cerita, dialog dan kontinuitas yang sudah dipilih pengguna.

## Landasan

- [TRY CGI: pengarahan kamera](https://materials.trycgi.xyz/p/move-camera-prompts)
- [TRY CGI: pipeline dan kontinuitas](https://materials.trycgi.xyz/p/secret-prompts-how-we-made-it)
- [Google: pengarahan Veo 3.1](https://cloud.google.com/blog/products/ai-machine-learning/ultimate-prompting-guide-for-veo-3-1)
- [Google Flow: fitur model](https://support.google.com/flow/answer/16352836?hl=en)

Ini sintesis materi publik yang diperiksa pada 28 Oktober 2026, bukan salinan prompt terkunci atau bukti uji generasi.
