# OpenMontage, Remotion dan HyperFrames

OpenMontage dipakai sebagai dependensi terpasang. Temukan root dari catatan proyek atau workspace, lalu baca AGENTS.md/AGENT_GUIDE.md dan PROJECT_CONTEXT.md miliknya sebelum memakai alat. Verifikasi Python environment dan tool yang diperlukan tanpa menjalankan generasi. Simpan commit OpenMontage dalam catatan produksi. Jangan memindahkan .env atau kredensial ke proyek skill.

Gunakan kontrak input aktual `VideoCompose` dari `tools/video/video_compose.py` dan registry OpenMontage. Terjemahkan daftar shot terpilih ke asset_manifest dan edit_decisions milik versi yang terpasang. Periksa schema dan contoh lokal sebelum memanggil execute; `production.json` milik skill bukan payload langsung alat ini. Tempatkan sumber komposisi dan hasil di folder proyek. Gunakan checkpoint OpenMontage hanya lewat API/helper aslinya.

## Pemilihan runtime

- FFmpeg untuk cut/trim/concat dan mix yang bisa dilakukan langsung. Simpan skrip edit yang bisa dijalankan ulang.
- Remotion untuk komposisi React, subtitle, teks dan grafis dengan timing frame. Pakai composer OpenMontage yang sudah ada; periksa package.json dan kontrak komposisinya. Simpan entry React, data shot, font, aset dan perintah preview/render yang benar-benar diuji.
- HyperFrames untuk komposisi HTML/GSAP. Baca skill `hyperframes` dan `hyperframes-cli` yang tersedia, serta `hyperframes-registry` sebelum membangun komponen yang sudah ada. Ikuti kontrak timeline deterministik, media dan fontnya. Jalankan check serta snapshot pada frame relevan sebelum render.

Pilih satu runtime utama sesuai kebutuhan proyek. Simpan keputusan itu; perubahan runtime perlu alasan dan persetujuan bila mengubah hasil/sumber yang disepakati. Jika runtime gagal, diagnosis dan laporkan blocker tanpa mengganti diam-diam.

Untuk edit manual, sertakan file sumber, data timeline, aset terpilih, subtitle dan audio terpisah jika digunakan. Gunakan path relatif dalam komposisi jika didukung agar proyek dapat dipindah. Buka preview yang tersedia dan hormati edit pengguna sebelum perubahan lanjutan. Verifikasi render dengan metadata serta frame awal/tengah/akhir dan batas cut. Periksa audio melalui Earshot. Preview sukses tidak membuktikan ekspor sukses. Ukuran, rasio, fps, durasi, audio dan keberadaan sumber edit harus sesuai brief.

## Dependensi dan lisensi

Integrasi ini memakai instalasi OpenMontage, bukan bundel salinan kode upstream. Referensi upstream yang ditinjau adalah commit `d21f5d4` dari https://github.com/calesthio/OpenMontage, berlisensi AGPL-3.0. Jika kelak menyalin/memodifikasi kode upstream ke distribusi, tinjau dan penuhi ketentuan lisensinya termasuk atribusi dan source yang relevan. Remotion, HyperFrames dan Earshot tetap mengikuti lisensi serta persyaratan masing-masing. Kemampuan runtime perlu diperiksa di mesin target; memasang skill tidak memasang seluruh runtime.
