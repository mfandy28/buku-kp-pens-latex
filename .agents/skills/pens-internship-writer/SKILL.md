---
name: pens-internship-writer
description: Menulis dan merevisi narasi akademik laporan KP PENS berdasarkan bukti proyek, termasuk paragraf, subbab, abstrak, dan kesimpulan. Gunakan untuk perubahan isi; bukan untuk layout saja atau audit tanpa revisi.
---

# Penulis Laporan KP PENS

## Tujuan

Mengembangkan narasi akademik yang menjelaskan pekerjaan penulis secara
jelas, konsisten, dan dapat ditelusuri ke bukti.

## Masukan dan rujukan

Temukan root yang memuat main_buku.tex. Baca AGENTS.md, bagian relevan
PROJECT_CONTEXT.md, berkas sasaran, dan sumber yang mendukung revisi.

Rujukan sesuai kebutuhan:
- tujuan dan batasan pada Bab I;
- konsep pada Bab III;
- implementasi dan hasil pada Bab IV;
- kesimpulan pada Bab V;
- refs/references.bib;
- manual, kode, catatan uji, dan koreksi pengguna yang tersedia.

Dokumen historis digunakan dengan statusnya, bukan sebagai sumber terbaru.

## Prosedur berbasis bukti

1. Tetapkan bagian dan tujuan revisi. Bedakan permintaan menyusun usulan
   dengan izin mengedit berkas.
2. Baca konteks sebelum/sesudah bagian sasaran dan bagian lain yang
   terdampak langsung.
3. Petakan klaim yang akan ditulis:
   - klaim;
   - sumber;
   - status kepastian;
   - kondisi atau batas penerapannya.
   Pemetaan ini dapat dilakukan dalam penalaran kerja; tidak perlu membuat
   berkas tambahan.
4. Pisahkan spesifikasi pabrikan, konfigurasi aktual, hasil pengujian,
   dan interpretasi. Pertahankan konflik yang belum terkonfirmasi.
5. Susun narasi sesuai fungsi bagian:
   - latar belakang: kondisi, kebutuhan, masalah, dan lingkup;
   - teori: konsep yang diperlukan untuk memahami pekerjaan;
   - rancangan: kebutuhan dan alasan pemilihan;
   - implementasi: perangkat, konfigurasi, dan alur;
   - pengujian: metode, kondisi, hasil, dan keterbatasan;
   - kesimpulan: jawaban terhadap tujuan berdasarkan hasil tersedia.
6. Tulis secara terbatas. Pertahankan informasi yang sudah benar dan
   hindari pengulangan yang tidak menambah penjelasan.
7. Periksa istilah, besaran, satuan, model, rentang, dan kondisi rumus.
   Periksa dukungan sitasi untuk klaim yang memerlukannya.
8. Cocokkan revisi dengan tujuan, batasan, pembahasan, dan kesimpulan
   yang terdampak.
9. Jika sumber LaTeX diubah dan verifikasi build diizinkan, gunakan
   prosedur latex-document-specialist.
10. Laporkan perubahan, sumber utama, dan informasi yang belum dapat
    dipastikan.

Jika bukti belum tersedia, jangan mengisi kekosongan dengan hasil atau
konfigurasi perkiraan. Kerjakan bagian yang tidak bergantung pada kekosongan
itu dan jelaskan konfirmasi yang diperlukan.

## Batasan

Ikuti batas perubahan pada AGENTS.md.

- Jangan membuat hasil pengujian, angka kinerja, konfigurasi, tanggal,
  atau kontribusi penulis yang tidak tersedia.
- Jangan menyajikan rencana pengujian sebagai pengujian yang sudah dilakukan.
- Jangan menyajikan rumus teoritis sebagai bukti implementasi atau kalibrasi.
- Jangan menggunakan spesifikasi umum untuk memastikan varian terpasang.
- Jangan mengubah struktur template untuk menyelesaikan masalah narasi.
- Jangan menganggap sumber yang berulang dalam naskah sebagai bukti baru.

## Kriteria keberhasilan

- Revisi memenuhi tujuan pengguna.
- Klaim penting dapat ditelusuri ke sumber dan status kepastian.
- Narasi membedakan rancangan, implementasi, hasil, dan interpretasi.
- Tidak muncul kontradiksi baru pada bagian yang terdampak.
- Data, gambar, tabel, label, dan referensi yang benar tetap dipertahankan.
- Keterbatasan bukti dinyatakan secara spesifik.
- Pemeriksaan teknis dilakukan sesuai izin dan dampak perubahan.
