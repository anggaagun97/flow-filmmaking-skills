---
name: flow-filmmaking
description: "Kelola produksi video dari brief atau video referensi sampai hasil edit melalui Google Flow MCP, OpenMontage, Remotion, HyperFrames dan Earshot. Gunakan untuk produksi lengkap, melanjutkan proyek, editing atau review footage/audio. Permintaan prompt atau aset saja tetap memakai skill Flow khusus."
metadata:
  version: "2.0.0"
---

# Flow Filmmaking

Gunakan Ponytail saat mengubah kode atau workflow. Kerjakan tahap yang diperlukan permintaan pengguna. Satu shot siap produksi langsung ke prompt dan eksekusi yang diminta. Proyek multi-shot memakai satu rencana shot. Revisi sempit hanya mengubah shot/aset terkait.

## Proyek dan kelanjutan

Baca catatan proyek yang ada sebelum membuat rencana baru. Gunakan folder `projects/<project-id>/` pada workspace produksi yang dipilih. Simpan nama proyek, URL/ID Flow, folder unduhan MCP, lokasi OpenMontage, runtime edit dan versi skill. Ikuti [kontrak proyek](references/project-contract.md) saat memulai atau melanjutkan produksi.

Gunakan satu daftar shot sebagai sumber timing, kamera, continuity, prompt, referensi, job ID dan hasil. Look proyek ditulis sekali dengan pengecualian per shot. Prompt final tetap memuat keputusan sinematik yang dibutuhkan model. Jangan mencetak ulang seluruh dokumen saat satu shot berubah.

## Pilih tahap

| Kebutuhan | Baca saat diperlukan |
|---|---|
| Video acuan atau pemeriksaan footage | [analisis video](references/video-analysis.md) |
| Naskah dan blocking multi-shot | `../flow-script-shotlist/SKILL.md` |
| Referensi identitas, properti atau set | `../flow-reference-assets/SKILL.md` |
| Prompt per shot | `../flow-video-prompts/SKILL.md` |
| Eksekusi Flow dan pemulihan job | [Flow MCP](references/flow-execution.md) |
| Editing, preview dan ekspor | [integrasi OpenMontage](references/editing.md) |
| Pemilihan, penilaian atau mix audio | [Earshot](references/audio.md) |

Skill khusus tetap dapat dipakai sendiri. Gunakan ID/nama yang sudah ada. Jangan memuat semua referensi di awal. Periksa ketersediaan alat hanya untuk tahap yang akan dijalankan.

## Selesai dan revisi

Catat hasil nyata, pemeriksaan gambar/audio, biaya yang diketahui dan batas verifikasi. Bedakan preview dari render final. Serahkan MP4 serta sumber edit dan aset terkait. Simpan status per shot agar pekerjaan bisa dilanjutkan tanpa merekonstruksi riwayat chat. Jangan menandai selesai berdasarkan keberadaan file saja; hasil tool, metadata dan pemeriksaan visual/audio harus sesuai.
