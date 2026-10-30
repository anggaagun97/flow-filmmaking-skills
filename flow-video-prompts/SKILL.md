---
name: flow-video-prompts
description: "Tulis, adaptasi atau perbaiki prompt video siap salin untuk Google Flow dengan Veo 3.1 dan Gemini Omni Flash 1.1. Gunakan untuk generasi dari teks, frame atau ingredients, dan revisi klip Omni; sertakan kontinuitas, kamera, suara dan negative prompt sesuai mode. Bukan untuk membuat naskah lengkap, gambar referensi, atau otomatis menjalankan generasi."
---

# Prompt video untuk Veo dan Omni di Google Flow

Terjemahkan brief atau shot list menjadi prompt yang mempertahankan cerita, identitas dan keputusan kamera pengguna. Tugas utamanya adalah menulis prompt; jangan mengklaim hasil render atau mengubah provider menjadi layanan lain.

## Tentukan konteks yang memengaruhi prompt

Gunakan model/varian, mode Flow, durasi, rasio, fungsi aset, tujuan shot, kontinuitas dan bahasa dialog dari konteks yang sudah ada. Jika ada shot list, pertahankan ID shot serta asetnya. Jangan membuat versi untuk dua model bila pengguna hanya meminta satu.

Bila pilihan model atau mode belum jelas, buat bagian pengarahan yang tidak bergantung pada pilihan tersebut dan tanyakan hanya hal yang benar-benar diperlukan untuk menyelesaikan prompt. Rutin seperti tone atau angle yang tidak ditetapkan dapat diasumsikan secara singkat.

Baca [profil model, negative prompt dan contoh](references/model-profiles.md) saat memilih mode, menulis pengecualian, atau menyusun revisi. Snapshot fitur di sana bertanggal; sebelum mengandalkan fitur produk yang dapat berubah, gunakan dokumentasi Flow terbaru atau bukti UI pengguna. Jangan menganggap kemampuan API sama dengan fitur Flow.

## Petakan mode dan peran gambar

- **Text-to-video:** tetapkan subjek, posisi, ruang, aksi, kamera, cahaya dan bunyi yang diperlukan.
- **Frame awal:** gambar menetapkan banyak informasi tampilan dan komposisi; teks mengarahkan perkembangan aksi, lingkungan dan kamera. Hindari deskripsi yang menentang gambar awal.
- **Frame awal-akhir:** jelaskan jalur perubahan yang masuk akal di antara keduanya. Jangan menjanjikan timing atau interpolasi sempurna.
- **Ingredients/references:** jelaskan fungsi karakter, lokasi, properti atau gaya. Aset identitas tidak harus ditiru sebagai komposisi frame awal.
- **Omni edit:** bedakan klip sumber dari gambar referensi; nyatakan perubahan dan unsur yang perlu dipertahankan.

Gunakan nama atau penanda aset yang benar-benar ada pada antarmuka. ID internal proyek bukan token Flow. Jangan mengarang upload atau menyalin tag API sebagai format wajib prompt Flow. Jika aset belum tersedia, nyatakan bahwa pemasangannya masih diperlukan.

Pada character sheet pengguna ini, close-up adalah acuan wajah tajam, sedangkan full shot depan/belakang adalah acuan tubuh dan pakaian dengan wajah diburamkan bila terlihat. Jangan mewariskan blur wajah dari sheet ke frame adegan atau video; arahkan identitas wajah dari panel close-up.

## Tulis pengarahan yang konkret

Jelaskan aksi utama, framing/angle, sasaran fokus, gerak serta arah kamera, kondisi awal dan akhir, lalu detail cahaya atau lingkungan yang memengaruhi shot. Untuk workflow pengguna ini, setiap prompt video harus mencantumkan focal length numerik (mm, acuan full-frame), ukuran shot yang dituju, camera angle, dan gerak kamera. Tulis focal length bersama hasil visual dan jarak relatif yang memungkinkan framing tersebut; angka mm saja tidak menentukan framing karena jarak kamera dan ukuran sensor ikut berpengaruh. Pilih lensa berdasarkan tujuan shot, bukan pemetaan kaku satu lensa untuk satu ukuran shot. Bedakan camera angle dari gerakan kamera, dan bedakan push-in fisik dari optical zoom. Tidak ada kewajiban memakai kamera mahal, film grain, hand-held atau paragraf panjang.

Contoh pengarahan kamera: `85mm lens, full-frame equivalent; medium close-up at seated eye level, frontal angle, camera far enough to include the shoulders and upper chest; a slow physical push-in with no optical zoom.` Untuk frame-to-video, frame awal tetap mengunci viewpoint dan crop awal: jangan memaksakan focal length atau angle baru yang menentang gambar. Bila angka lensa hanya mengarahkan look karena kamera gambar tidak diketahui, nyatakan sebagai lens look dan pertahankan komposisi frame awal. Perubahan framing atau angle yang penting perlu dirancang pada frame awal terlebih dahulu.

Jaga hubungan sebab-akibat yang penting: tangan menyentuh dan menopang benda, benda tidak berubah bentuk tanpa maksud, bayangan/refleksi masuk akal, angin memengaruhi unsur terkait. Pilih detail natural yang relevan, bukan daftar efek realisme pada setiap shot.

Pisahkan hal tetap dari aksi yang berubah: wajah, rambut, pakaian, desain properti, tata ruang dan sumber cahaya. Jangan menjanjikan bahwa teks continuity lock pasti mengunci identitas atau suara secara identik.

Jika satu take diinginkan, tegaskan kontinuitas tanpa cut; terutama pada Omni yang dapat membuat beberapa shot. Untuk multi-shot, berikan urutan atau timestamp secukupnya sesuai durasi. Jangan meminta cut sambil melarang semua cut.

## Standar cinematic wajib pengguna

Setiap prompt generasi video, termasuk tiap shot dalam rangkaian multi-shot, harus menjelaskan gerak kamera (atau static), focal length numerik acuan full-frame, framing dan angle, aperture numerik beserta target fokus/bokeh/DoF, referensi film stock beserta karakter tampilannya, susunan lighting yang membentuk subjek, serta atmosfer dan dampaknya ke adegan/karakter. Pilih nilai yang sesuai cerita; udara bersih, deep focus, high-key atau kamera diam tetap sah. Jangan menyamakan cinematic dengan gelap, bokeh kuat atau grain berat.

Baca [pengarahan cinematic dan contoh](references/cinematic-direction.md) saat menulis atau merevisi prompt. Lengkapi unsur yang belum ditentukan melalui asumsi kreatif yang masuk akal; jangan menunda draft dengan pertanyaan rutin. Pertahankan frame awal dan keputusan yang tidak diminta berubah pada edit sempit; metadata optik yang tidak diketahui ditulis sebagai look, bukan fakta kamera asli.

Default prompt adalah bahasa alami lengkap. Kode slash/no-slash hanya alat bantu ringkas bila pengguna meminta, bukan sintaks resmi atau jaminan hasil. Jangan membuang keputusan visual wajib demi kode. Sebelum menyerahkan, periksa konflik antar-gerak, framing/lensa/jarak, fokus/aksi, cahaya/atmosfer dan kontinuitas antar-shot.

## Sesuaikan cara penyampaian dengan tugas

**Veo generasi:** deskripsikan shot yang dapat divisualisasikan, misalnya kamera/framing, subjek, aksi, konteks/cahaya, suara, serta kontinuitas. Urutan ini alat menyusun ide, bukan sintaks wajib.

**Omni generasi:** nyatakan maksud visual dan interaksi, kemudian kamera dan hal penting yang dipertahankan. Lengkapi detail yang benar-benar mengurangi ambiguitas. Jangan menganggap Omni selalu harus diberi prompt pendek atau Veo selalu harus diberi prompt panjang.

**Omni edit:** minta perubahan spesifik lalu sebut apa yang harus tetap. Hindari menulis ulang seluruh adegan ketika hanya satu unsur yang perlu diperbaiki. Nilai kembali bagian yang diminta tetap setelah pengguna melihat hasil.

Default penjelasan mengikuti bahasa pengguna. Prompt visual dapat ditulis dalam bahasa Inggris sebagai titik awal, kecuali pengguna menginginkan bahasa lain. Pertahankan bahasa dan kata-kata dialog yang sudah dipilih; jelaskan siapa berbicara, gaya performa, dan ambience bila relevan. Jangan otomatis menambahkan musik, narasi atau subtitle.

## Negative prompt

Pertahankan daftar hal yang tidak diinginkan pengguna. Pilih pengecualian yang relevan, dan hapus konflik dengan arah positif. Untuk shot hand-held, larangan seluruh camera shake berlawanan dengan tujuan; larangan goyangan berlebihan mungkin lebih sesuai.

Bila field negative terpisah benar-benar tersedia dan didukung, tulis daftar unsur yang dikecualikan. Bila masuk prompt utama, terutama Omni, tulis kalimat larangan yang jelas. Judul "Negative prompt" sendiri tidak membuat field atau parameter khusus.

## Keluaran

Berikan setup Flow singkat, pemetaan aset yang diperlukan, prompt siap salin per shot, serta daftar pengecualian. Jika pengecualian sudah dimasukkan ke prompt utama, jelaskan itu agar pengguna tidak perlu menempel bagian yang sama dua kali.

Untuk revisi, jelaskan perubahan utama dan berikan prompt penggantinya atau instruksi edit yang tepat. Periksa konflik sebelum menyerahkan hasil. Evaluasi sesuai kegagalan yang benar-benar dilihat: identitas, framing, aksi, kamera, properti, cahaya, cut tidak diinginkan atau audio. Jangan menyatakan prompt telah terbukti berhasil sebelum ada hasil generasi yang diperiksa.

## Batas eksekusi dan pengulangan

Skill ini menulis prompt; jalankan generasi hanya bila pengguna juga meminta eksekusi. Koreksi format atau pembahasan hasil bukan izin otomatis untuk render ulang. Penggabungan klip pada workflow pengguna ini dilakukan manual.

Saat eksekusi diminta: gunakan satu varian per shot dan retry otomatis 0 sebagai awal, tetapkan jumlah generasi yang direncanakan dan biaya yang diketahui. Bila integrasi gagal atau respons ambigu, hentikan submit berikutnya dan cocokkan job dengan aset proyek sebelum mengulang; status gagal pada MCP tidak membuktikan provider belum membuat atau menagih klip. Ambil hasil yang sudah ada lewat download. Diagnosis MCP tidak boleh menjadi rangkaian tes generasi berbayar. Rekonsiliasi saldo dan jumlah aset setelah ketidakpastian sebelum melanjutkan. Batas pengeluaran mencakup seluruh percobaan, bukan hanya klip terpilih; berhenti sebelum batas terlampaui. Buat revisi terarah hanya untuk kegagalan yang menghalangi tujuan shot, dalam ruang iterasi yang telah diizinkan pengguna.
