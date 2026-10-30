# Profil model dan penerapan di Flow

## Fitur: snapshot 28 Oktober 2026

Sumber utama untuk produk adalah [Google Flow Help](https://support.google.com/flow/answer/16352836?hl=en). Saat diperiksa: Veo 3.1 Fast dan Quality menyediakan klip 4/6/8 detik serta first/last frames; ingredients tercantum untuk Fast pada 8 detik, tidak untuk Quality. Omni Flash 1.1 mencantumkan 4/6/8/10 detik, frames, ingredients dan edit video. Omni Extend masih coming soon di Flow, walaupun API membahas extension.

Ini catatan bertanggal, bukan aturan permanen. Ikuti UI aktual atau dokumentasi baru ketika berbeda. Jangan merencanakan klip 27-30 detik hanya karena contoh TRY CGI menggunakan Seedance. Jangan menjanjikan fitur untuk akun pengguna tanpa dasar.

## Negative input dan pengecualian pada teks utama

Untuk field negative tersendiri yang benar-benar didukung, contoh daftar:

```text
camera shake, overexposure, blown-out highlights, captions
```

Untuk prompt utama, contoh penerapan yang baru ditulis:

```text
Keep the camera stable and preserve detail in bright areas.
No camera shake, no additional people, no captions or dialogue.
```

Sesuaikan dengan shot; contoh ini tidak cocok bila adegan membutuhkan hand-held, kerumunan, tulisan atau percakapan. Pada negative field, [panduan Google Cloud](https://docs.cloud.google.com/gemini-enterprise-agent-platform/models/video/video-gen-prompt-guide#negative-prompts) menyarankan daftar unsur. [Dokumentasi Omni](https://ai.google.dev/gemini-api/docs/omni#gemini-omni-flash-prompt-guide) tidak menyediakan parameter negative terpisah di API, tetapi mengizinkan larangan sederhana dalam teks utama. Hal itu tidak membuktikan semua akun Flow memiliki negative field.

## Contoh: frame awal sudah benar

Asumsikan frame awal benar-benar memperlihatkan pria duduk memegang amplop dalam pencahayaan window key dan look daylight yang sesuai. Angka optik berikut adalah look, bukan metadata gambar. Contoh baru:

```text
The seated man opens the envelope, pauses when he finds it empty,
then raises his eyes toward the person opposite him. Gently push
in from the starting chest-up framing to a close-up of his reaction.
Use an 85mm full-frame-equivalent lens look at seated eye level,
camera far enough for the starting chest-up crop; f/2.8 aperture look,
near eye in focus, shallow depth and restrained soft background bokeh.
Preserve the initial frame's viewpoint, identity, wardrobe and envelope.
Use a Kodak VISION3 250D-inspired natural daylight palette consistent
with the source frame, fine grain and controlled highlights. Preserve
the large soft side-window key shaping the cheek, with subtle fill on
the shadow side. Clear indoor air; a faint breeze lifts only the loose
flap while he holds the envelope. Keep the established light direction.
One continuous shot. Sound: wind and paper rustling.
No scene cuts, music, dialogue or captions.
```

Jika subjek atau properti tidak ada pada frame awal, jangan menggunakan contoh ini sebagai bukti bahwa model akan menambahkannya. Perbaiki frame atau jelaskan perubahan sesuai mode.

## Contoh: edit hanya cahaya dengan Omni

```text
Reduce the overexposure and restore detail in the sky and light
clothing. Keep the character, action, camera movement, framing
and existing audio unchanged.
```

Instruksi mempertahankan membantu mengarahkan, bukan jaminan bahwa bagian lain tidak berubah. Jika tujuannya mengubah audio, bedakan itu dari permintaan mempertahankan audio.

## Bukti dan ruang interpretasi

- [Veo 3.1: panduan Google](https://cloud.google.com/blog/products/ai-machine-learning/ultimate-prompting-guide-for-veo-3-1): pengarahan visual, aksi, konteks, suasana dan suara; bukan ketentuan urutan kata wajib.
- [Omni: panduan DeepMind](https://deepmind.google/models/gemini-omni/prompt-guide/): maksud visual, kamera dan revisi spesifik melalui bahasa alami.
- [GitHub resmi Google](https://github.com/google-gemini/gemini-skills/blob/main/skills/gemini-omni-flash-api/SKILL.md): single shot, timing, suara, larangan sederhana dan edit terarah. Tidak memerlukan skrip API untuk drafting Flow.
- [Flow: pembuatan](https://support.google.com/flow/answer/16353334?co=GENIE.Platform%3DDesktop&hl=en) dan [editing](https://support.google.com/flow/answer/16935718?hl=en): rujukan workflow produk.

Default satu aksi utama dan satu tujuan kamera adalah strategi awal untuk memudahkan evaluasi, bukan batas kemampuan model. Tidak ada klaim bahwa JSON, bahasa Inggris untuk semua dialog, focal length tertentu atau satu susunan prompt selalu unggul. Contoh adalah hasil sintesis; belum merupakan uji generasi.
