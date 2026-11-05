# Eksekusi Flow MCP

Temukan tool Flow yang benar-benar tersedia. Baca schema aktual sebelum pemakaian. `flow_status` ringan untuk mengidentifikasi sesi/proyek; mode rinci dipakai saat saldo/quote diperlukan. Jika belum ada proyek aktif atau identitasnya berbeda dari rencana, selesaikan pemilihan proyek sebelum submit. Parameter `project` menamai folder unduhan dan tidak memilih proyek web.

Gunakan aturan cache dan nama pada `../../flow-reference-assets/SKILL.md`. Pada proyek yang sama dengan indeks tersedia, pakai `asset:<judul-persis>` tanpa inventarisasi atau upload ulang. Baca daftar aset sekali ketika proyek berubah atau belum ada indeks. Upload hanya aset yang belum tersedia, simpan judul aktual yang dikembalikan. Jangan mengklaim rename berhasil jika MCP tidak mendukungnya.

## Sebelum submit

- Cocokkan model label, mode, rasio, durasi dan resolusi dengan schema/tool saat ini. Jangan biarkan pilihan model mengikuti UI yang tidak diketahui. Durasi Veo dan opsi Omni diverifikasi dari tool saat eksekusi.
- Pisahkan ingredients dari first/last frame. Jika Composer tidak mendukung keduanya, selesaikan frame adegan terlebih dahulu atau gunakan jalur tool yang mendukung kombinasi tersebut.
- Tetapkan `variants: 1`, `retries: 0` secara eksplisit kecuali pengguna sudah mengizinkan lainnya. Tentukan `max_credits` tiap scene dan total komitmen batch yang masih masuk anggaran. Quote adalah batas/prediksi, bukan bukti biaya aktual.
- Beritahu jumlah klip dan perkiraan kredit sebelum submit. Otorisasi produksi yang sudah jelas tidak perlu diminta ulang. Hentikan saat quote tidak diketahui atau melampaui batas yang diizinkan.
- Batch shot independen yang siap dalam satu panggilan. Simpan urutan scene ke ID shot. Shot yang bergantung pada hasil sebelumnya menunggu hasil yang sudah diterima, kecuali chaining eksplisit sesuai brief.

## Job, tunggu dan hasil

Simpan job ID segera setelah diterima. Gunakan `flow_wait` dengan ID job terkait sampai terminal, bukan polling status/daftar aset berkali-kali. Tool dapat berjalan serial dengan jeda bawaan; jangan melaporkan batch sebagai render paralel. Gunakan kualitas unduhan original sebagai awal, upscale saat diminta atau diperlukan keluaran akhir.

Respons timeout/ambigu berarti unknown. Periksa job yang sudah ada dan, bila perlu, aset proyek sekali untuk pemulihan. Jangan menyimpulkan tidak ditagih dari error MCP. Jangan memanggil retry seluruh antrean. Retry terarah hanya untuk job yang dipastikan gagal, dalam jumlah dan anggaran yang diizinkan. Unduh hasil yang sudah ada lewat `flow_download` tanpa regenerasi.

Catat path hasil MCP aktual. Jika berbeda dari folder proyek, pindahkan/salin file ke assets/video atau assets/images setelah memverifikasi file, lalu catat sumber dan tujuan. Pertahankan hasil asli sampai salinan terverifikasi. Biaya aktual yang tidak dilaporkan ditandai unknown. Periksa identitas, aksi, framing dan sambungan sebelum menerima shot.
