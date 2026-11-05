# Kontrak proyek v2

Pakai satu penulis catatan proyek pada satu waktu. Jika ada proses produksi aktif, lanjutkan atau tunggu proses itu sebelum submit baru. File dicatat setelah hasil tool diketahui. Saat menulis JSON, tulis file sementara di folder yang sama lalu replace secara atomik; pertahankan file terakhir yang valid saat operasi gagal.

Struktur minimal mengikuti folder kerja OpenMontage. Buat hanya artefak yang diperlukan tahap aktif.

```text
projects/<project-id>/
  project.json
  artifacts/production.json
  assets/images/
  assets/video/
  assets/audio/
  edits/
  renders/
```

`project.json` mempertahankan field milik OpenMontage jika proyek sudah ada. Catat tambahan integrasi di `artifacts/production.json`, bukan mengubah schema checkpoint OpenMontage. Jangan menimpa artefak lama atau menyatakan catatan baru otomatis kompatibel dengan Backlot.

`production.json` berisi field berikut sesuai tahap yang sudah berjalan.

| Field | Isi |
|---|---|
| schema_version, skill_version | `2`, `2.0.0` |
| project_id, title | ID folder tetap dan judul yang jelas |
| flow | project_url/id, project_name, mcp_download_project, asset_index_project_id |
| runtimes | openmontage_root dan commit yang dipakai, render_runtime, source_entry |
| look | Keputusan sinematik bersama, continuity dan preferensi pengguna |
| assets | ID, nama/versi, path lokal, judul Flow aktual, peran dan status |
| shots | ID tetap, durasi edit/klip, aksi, keputusan kamera, pengecualian look, prompt final, asset IDs |
| attempts per shot | request settings, job ID, status, quote/batas/biaya aktual yang diketahui, path hasil dan catatan QA |
| budget | unit kredit atau mata uang, batas total yang diizinkan, pengeluaran diketahui dan komitmen belum selesai |
| next_action | Langkah berikutnya yang konkret dan blocker jika ada |

Status shot bergerak dari planned ke ready, queued, running, generated, reviewed dan accepted. Gunakan failed atau unknown ketika sesuai. Unknown menahan submit pengganti sampai job direkonsiliasi. Revisi menyimpan attempt sebelumnya dan menandai hasil yang dipilih. Jangan menjumlahkan kredit Flow dan USD API dalam satu angka.

Catatan pemakaian aset berindeks proyek Flow, bukan akun atau judul proyek saja. Proyek yang sama dengan indeks valid memakai nama yang tercatat. Pergantian proyek atau pemulihan aset hilang memperbarui indeks sesuai aturan skill aset. Jika URL/ID tidak tersedia, minta identitas proyek yang dapat diverifikasi sebelum generasi.

Migrasi proyek lama dilakukan saat digunakan. Pertahankan ID, nama aset dan file yang tersedia; tambahkan field yang dibutuhkan saja. Jangan membuat ulang footage karena format catatan berubah. Rahasia, API key dan konfigurasi akun tetap di penyimpanan lokal yang sesuai dan di luar repo.
