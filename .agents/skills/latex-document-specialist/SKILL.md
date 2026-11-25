---
name: latex-document-specialist
description: Mengelola gambar, tabel, caption, penomoran, referensi silang, layout A5, dan kompilasi pada proyek LaTeX PENS yang sudah berjalan. Gunakan untuk pekerjaan penyajian dokumen; bukan untuk menulis ulang narasi.
---

# Spesialis Dokumen LaTeX PENS

## Tujuan

Menerapkan perubahan penyajian yang terbatas dan menjaga integritas isi,
konfigurasi template yang disetujui, serta kesesuaian sumber dan PDF.

## Rujukan

Baca AGENTS.md, konfigurasi pada PROJECT_CONTEXT.md, dan berkas terkait.

Periksa sesuai kebutuhan:
- main_buku.tex;
- Makefile dan .latexmkrc;
- config/packages.tex, formatting.tex, fonts.tex, migration.tex;
- formats/format_buku.tex;
- konfigurasi LaTeX Workshop yang benar-benar aktif;
- macro gambar/tabel dan manual paket terkait.

Jika dokumentasi sintaks/API/tool diperlukan, gunakan sumber resmi dan
Context7 sesuai instruksi global. Jangan memasang alat tambahan.

## Prosedur perubahan

1. Tentukan lingkup: gambar, tabel, caption, referensi, layout, atau build.
2. Periksa sumber serta PDF yang tersedia. Bedakan nomor halaman tercetak
   dan urutan halaman PDF.
3. Identifikasi pengendali lokal/global dan dependensi yang terdampak.
4. Terapkan perubahan minimum yang diizinkan.
5. Periksa sesuai tugas:
   - gambar: kecocokan file, orientasi, rasio, ukuran, dan caption;
   - tabel: data, satuan, kolom, lebar, dan pemenggalan;
   - referensi: label unik dan tujuan yang benar;
   - layout: margin, header/footer, jarak, dan hubungan judul dengan isi.
6. Lakukan kompilasi hanya jika diizinkan, mengikuti prosedur di bawah.
7. Periksa log dan halaman PDF yang terdampak, termasuk halaman sekitar
   bila terjadi pergeseran.
8. Perbarui PDF yang dibagikan hanya setelah hasil diverifikasi.
9. Laporkan perubahan, metode verifikasi, dan masalah yang masih tersisa.

Audit/perancangan read-only tidak menjalankan prosedur yang menulis berkas.

## Gambar dan tabel

- Gunakan aset pengguna yang dapat diakses sebagai file dan periksa
  kecocokannya sebelum menyisipkan.
- Jangan mengganti aset dengan alternatif material tanpa persetujuan.
- Pertahankan orientasi tegak, rasio aspek, dan caption rata tengah.
- Pertahankan label agar referensi silang tidak rusak.
- Untuk beberapa foto dalam satu nomor gambar, gunakan susunan LaTeX
  dan satu caption bila sesuai permintaan.
- Bedakan ilustrasi/gambar generatif dari foto bukti implementasi.
- Pertahankan isi sel dan satuan ketika memperbaiki tabel.
- Jangan menambahkan kembali keterangan sumber penulis yang telah dihapus.

## Pemilihan jalur kompilasi

Sebelum menjalankan build:
1. Baca Makefile dan .latexmkrc yang aktual.
2. Periksa sistem operasi, shell, executable, PATH, dan working directory.
3. Pastikan root kerja memuat main_buku.tex dan .latexmkrc.
4. Pilih jalur yang sesuai dengan lingkungan yang tersedia.

Konfigurasi baseline:
- Inti target buku pada Makefile adalah:
  latexmk -pdf main_buku.tex
- .latexmkrc menetapkan pdflatex, BibTeX, serta output/auxiliary di build/.
- Makefile juga memakai utilitas bergaya POSIX dan menyalin PDF ke
  output/ dengan nama bertanggal.
- TinyTeX tersedia pada profil pengguna Windows yang tercatat di konteks.

Pilihan:
- Gunakan make buku jika make, shell, utilitas pendukung, dan perilaku
  target tersebut sesuai dengan tugas.
- Jika lingkungan Makefile tidak tersedia, jalankan inti build dengan
  latexmk dari root proyek sehingga .latexmkrc tetap digunakan.
- Jika executable belum ditemukan melalui PATH, gunakan lokasi instalasi
  yang telah diperiksa atau penyesuaian sementara pada proses tersebut.
  Jangan mengubah konfigurasi global secara otomatis.
- Jangan mengganti mesin, output directory, atau opsi proyek tanpa alasan.

Perintah shell, environment variable, dan workaround locale tidak universal.
Gunakan hanya jika sesuai lingkungan dan ada masalah yang membutuhkannya.

## Opsi tambahan dan kegagalan

Mulai dengan build biasa sesuai konfigurasi proyek.

Opsi kompilasi paksa hanya digunakan setelah ada alasan yang teridentifikasi,
misalnya aset baru pada cabang IfFileExists tidak terdeteksi oleh dependensi.
Jelaskan alasannya; jangan menjadikannya opsi default.

Jika build gagal:
- periksa exit code dan bagian log yang relevan;
- bedakan masalah sumber, dependensi, executable, dan lingkungan;
- perbaiki penyebab yang berada dalam lingkup tugas;
- jangan menghapus hasil kerja atau memasang paket secara otomatis.

Jangan menjalankan make cleanall atau migration/migrate.py.
Jangan menggunakan pembersihan massal sebagai percobaan perbaikan.

## Verifikasi dan publikasi PDF

Periksa:
- error LaTeX/BibTeX;
- undefined reference/citation;
- label ganda;
- Overfull atau float melebihi halaman;
- aset hilang dan placeholder yang seharusnya terisi;
- caption, penomoran, dan referensi silang;
- ukuran A5 serta konfigurasi template yang disetujui.

Gunakan label aktual pada .aux bila diperlukan. Macro GambarLaporan dan
longtblr dapat menghasilkan label yang tidak terlihat sebagai label literal
pada pemeriksaan teks sederhana.

Nilai Underfull, substitusi font, dan peringatan caption berdasarkan dampaknya
dan perbandingan dengan baseline. Jangan mengubah isi untuk membungkam warning.

PDF build:
build/main_buku.pdf

PDF yang selama ini dibagikan:
output/Laporan_KP_Fandy_Fadhil_Migrasi_LaTeX.pdf

Target make buku dapat menghasilkan salinan bertanggal sebelum review visual.
Keberadaan salinan itu tidak berarti PDF sudah diverifikasi. Perbarui salinan
yang dibagikan setelah pemeriksaan selesai.

Jika output terkunci, laporkan tanpa menghapus paksa.
Jangan menyunting PDF hasil sebagai pengganti perbaikan sumber LaTeX.

## Kriteria keberhasilan

- Perubahan memenuhi tugas dan mempertahankan konfigurasi template.
- Isi, label, dan referensi yang benar tetap utuh.
- Build berhasil jika build baru dijalankan.
- Tidak ada error, referensi hilang, label ganda, atau Overfull baru.
- Halaman yang terdampak telah diperiksa secara visual bila memungkinkan;
  keterbatasan pemeriksaan dinyatakan.
- PDF yang dibagikan sesuai hasil build yang telah diverifikasi.
- Opsi tambahan dan peringatan tersisa memiliki alasan yang jelas.
