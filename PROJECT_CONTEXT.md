# Konteks Proyek Laporan Kerja Praktik PENS

Dasar konteks: audit Tahap 1, rancangan final Tahap 2, dan konfirmasi pengguna.
Tanggal baseline: 19 November 2026.

Dokumen ini menyimpan konteks dan status bukti. Dokumen ini bukan bukti
pengujian lapangan, persetujuan pembimbing, atau izin perubahan.
Periksa berkas aktual sebelum menggunakan informasi yang dapat berubah.

## 1. Status kepastian

- U — Dikonfirmasi langsung oleh pengguna.
- F — Terverifikasi sebagai keadaan berkas proyek.
- P — Didukung dokumentasi primer untuk model/karakteristik tertentu.
- D — Tercatat dalam draft, belum diverifikasi terhadap kondisi aktual.
- V — Belum lengkap, berkonflik, atau membutuhkan konfirmasi.

Status dapat digabungkan. Contoh:
- U/F: dikonfirmasi pengguna dan sudah tercatat dalam berkas.
- P/V: spesifikasi model diketahui, kesesuaiannya dengan unit terpasang
  masih harus diperiksa.
- D/V: uraian tersedia, bukti aktual belum tersedia.

Status F tidak membuktikan kondisi lapangan.
Status P tidak membuktikan model atau pengaturan perangkat terpasang.

## 2. Daftar sumber

### Sumber pengguna

- U01: koreksi program studi D3, Departemen Teknik Elektro, koordinator KP,
  kepala program studi, dan NIP masing-masing.
- U02: istilah “mesin cutting”, “HMI”, dan satu nama aplikasi HMI;
  tanpa AC90/AC95, “HMI lokal”, atau hmi_v2.
- U03: monitoring cutting dikerjakan Fandy; monitoring panel dikerjakan
  Fadhil dan juga berbasis Raspberry Pi.
- U04: cetak bolak-balik, ukuran A5, caption gambar rata tengah,
  diagram tegak; pengguna pernah meminta Gambar 4.1 pada halaman 39.
  Nomor halaman dapat bergeser setelah perbaikan tata letak menyeluruh.
- U05: satu transduser untuk satu fasa; tiga transduser untuk tiga fasa.
- U06: dua jenis keluaran transduser, 4–20 mA dan 0–5 V, karena
  keterbatasan ketersediaan barang; keduanya diterima modul Waveshare.
- U07: pengguna mengonfirmasi bahwa proyek menggunakan tepat satu
  adapter USB-to-RS485.
- U08: pengguna mengonfirmasi RTD Converter menggunakan Slave ID 1
  dan Waveshare Modbus RTU Analog Input 8CH menggunakan Slave ID 2.
- U09: penghapusan keterangan sumber penulis dan referensi yang sebelumnya
  ditolak dalam percakapan proyek.
- U10: backup proyek sudah tersedia.
- U11: pada 19 November 2026, pengguna mengonfirmasi bahwa kedua perangkat
  dihubungkan secara paralel pada satu bus RS485 dan berkomunikasi
  melalui adapter USB-to-RS485 yang sama.
- U12: dalam persetujuan implementasi Tahap 3, pengguna menegaskan
  Raspberry Pi 5 sebagai komputer utama sistem monitoring.

### Sumber proyek

- F01: config/variables.tex — identitas dan judul yang tersimpan.
- F02: chapters/bab1.tex sampai chapters/bab5.tex — naskah aktif.
- F03: pages/ — halaman awal dan lampiran.
- F04: assets/gambar/ dan assets/diagrams/ — foto dan diagram.
- F05: main_buku.tex, config/, formats/, .latexmkrc, Makefile,
  dan konfigurasi LaTeX Workshop — penyajian dan build.
- F06: refs/references.bib — metadata pustaka yang tersimpan.
- F07: PDF, .aux, dan log dalam build/, serta PDF dalam output/ —
  hasil kompilasi pada baseline audit.
- D01: Draf_Laporan_KP_Fandy_Fadhil_Monitoring_Cutting_A4_Revisi_2.docx —
  sumber uraian awal.
- D02: BUKU_KP_FIX_DIKUMPULKAN_2123600018.pdf —
  acuan konteks perusahaan; bukan bukti hasil proyek penulis.
- H01: migration/ — ekstraksi, pemetaan, skrip, dan catatan historis.

### Sumber teknis primer yang dirujuk

- P01: SMC, manual ZSE30A(F)/ISE30A, citation key smcise30a:
  https://www.smcworld.com/upfiles/_manual/e/PSxx-OML0003.pdf
- P02: SMC, katalog PFMB, citation key smcpfmb:
  https://ca01.smcworld.com/catalog/BEST-5-6-en/pdf/pfmb_en.pdf
- P03: OMEGA, manual M2897, citation key pt100reference:
  https://assets.omega.com/manuals/M2897.pdf
- P04: Waveshare Modbus RTU Analog Input 8CH, citation key waveshare:
  https://www.waveshare.com/wiki/Modbus_RTU_Analog_Input_8CH
- P05: Modbus Application Protocol Specification V1.1b3,
  citation key modbus2012; metadata dan tautan tersimpan di F06.

Sumber di atas pernah digunakan dalam penyusunan. Untuk klaim baru,
periksa kembali bagian manual yang relevan dan kecocokan model.
Keberadaan URL dalam daftar ini tidak menggantikan pemeriksaan sumber.

## 3. Identitas proyek

Root:
D:/Kerja Praktek/Report/Laporan KP/buku-kp-pens-latex-main

Judul yang tersimpan:
Perancangan dan Implementasi Sistem Monitoring Mesin Cutting dan Panel
Berbasis Industrial Internet of Things (IIoT) Menggunakan Raspberry Pi

Penulis:
- Muhammad Fandy Anggriawan — 2124500045.
- Muhammad Fadhil Abdillah — 2124500053.

Program studi: D3 Teknik Elektronika.
Departemen: Departemen Teknik Elektro.
Institusi: Politeknik Elektronika Negeri Surabaya.

Perusahaan: PT XYZ, nama disamarkan.
Lokasi yang tercatat: Kecamatan Ngoro, Kabupaten Mojokerto, Jawa Timur.
Penempatan yang tercatat: Divisi Maintenance.
Periode yang tercatat: 1 Juli–31 Desember 2026.

Sumber/status:
- Judul, nama, NRP, lokasi, dan periode: F01/F.
- Jenjang dan departemen: U01 + F01/U,F.
- Penempatan: F02 + D01/D,F.
- Penyembunyian nama perusahaan: instruksi pengguna + F01/U,F.

Identitas yang tersimpan:
- Dosen pembimbing:
  Dr. Ir. Agus Indra Gunawan, S.T., M.Sc.
  NIP 197608212001121002. [F01/F]
- Koordinator KP:
  Hanny Megawati Rosalinda, S.T., M.T., M.Sc.
  NIP 199301262022032009. [U01 + F01/U,F]
- Kepala Program Studi:
  Madyono S.ST., MT.
  NIP 196904251992031001. [U01 + F01/U,F]
- Pembimbing lapangan: Imsyar Lubis Tandika. [F01 + D01/D,F]
- Senior Manager: Dwi Jasmianto. [F01 + D01/D,F]

Jangan menganggap identitas yang tersimpan sebagai pemeriksaan jabatan
terkini. Perubahan memerlukan koreksi pengguna atau bukti yang sesuai.

## 4. Ketentuan dan pembagian pekerjaan

- Gunakan istilah “mesin cutting” dan “HMI”. [U02/U]
- Jangan menggunakan AC90/AC95, “HMI lokal”, atau hmi_v2. [U02/U]
- Cutting merupakan lingkup Fandy. [U03/U]
- Panel merupakan lingkup Fadhil dan berbasis Raspberry Pi. [U03/U]
- Program node dan dashboard panel telah diberikan serta ditelaah; konfigurasi operasional dikonfirmasi satu Raspberry Pi untuk empat panel di Power Room melalui UART--RS485. [U15 + C01 + C02/U,F]
- A5, cetak bolak-balik, caption rata tengah, diagram tegak. [U04/U]
- Jangan menambahkan kembali keterangan sumber penulis atau referensi
  yang sudah ditolak. [U09/U]

## 5. Perangkat: spesifikasi dan keadaan aktual

### 5.1 Raspberry Pi, layar, dan catu daya

Komputer utama monitoring cutting dan panel adalah Raspberry Pi 5. Kesamaan model kedua proyek dikonfirmasi pengguna pada 20 November 2026. Penyebutan model pada naskah dibatasi di bagian 4.1.7.1; bagian lain menggunakan Raspberry Pi. [U12 + U19 + F02/U,F]

Informasi dalam naskah:
- Touch Display 7 inci melalui DSI.
- Catu daya 5 VDC untuk Raspberry Pi.
- Catu daya 24 VDC untuk perangkat pengukuran/alarm sesuai uraian.

Sumber/status: F02 + F04 + D01/D,F.

Belum terkonfirmasi:
- Model/revisi layar terpasang.
- Model, kapasitas arus, pengaturan tegangan, dan distribusi daya aktual.
- Kesesuaian seluruh foto dengan unit lapangan.

Status: V. Foto produk tidak membuktikan pemasangan atau kapasitas aktual.

### 5.2 PT100 dan konverter RTD–RS485

Spesifikasi/karakteristik:
- PT100 menghasilkan perubahan resistansi.
- Nilai nominal 100 ohm pada 0 derajat Celsius.
- Sekitar 138,5 ohm pada 100 derajat Celsius untuk karakteristik PT100
  yang dirujuk. [P03/P]
- Label sensor pada foto mencantumkan -200 hingga 420 derajat Celsius.
  [F04/F, terbatas pada label foto]

Konfigurasi:
- PT100 terhubung ke konverter RTD–RS485 dalam naskah. [F02 + D01/D,F]
- Slave ID konverter RTD adalah 1. [U08/U]
- Naskah menyebut data suhu melalui Modbus RTU/RS485. [F02 + D01/D,F]

Belum terkonfirmasi:
- Model konverter, rentang yang didukung, register, tipe data,
  signedness, faktor skala, dan konfigurasi sensor.
- Rentang sistem lengkap tidak dapat disamakan dengan rentang label probe.
Status: V.

### 5.3 Transduser arus

Konfigurasi yang dikonfirmasi:
- Satu transduser mengukur satu fasa.
- Tiga transduser diperlukan untuk R, S, dan T. [U05/U]
- Digunakan jenis keluaran 4–20 mA dan 0–5 V.
- Pemilihan dua jenis karena ketersediaan barang.
- Keduanya diterima modul Waveshare dengan konfigurasi yang sesuai.
  [U06/U]

Label foto:
- Unit keluaran 4–20 mA pada Gambar 4.5 mencantumkan masukan
  0–20 A AC dan catu daya 24 VDC. [F04/F]

Belum terkonfirmasi:
- Batas ukur dan catu daya varian 0–5 V.
- Model dan pemetaan masing-masing varian pada fasa/mesin.
- Pengaturan kanal dan kalibrasi aktual.
Status: V.

Jangan menerapkan batas 20 A pada seluruh unit hanya karena satu foto
menunjukkan batas tersebut.

### 5.4 Sensor tekanan

Model pada naskah: SMC ISE30A-01-D. [F02/D,F]

Spesifikasi model:
- Kode D menyediakan keluaran sakelar NPN dan keluaran arus analog.
- 4–20 mA berkorespondensi dengan 0–1 MPa atau 0–10 bar.
- Rentang nominal mencakup -0,1 hingga 1 MPa; keluaran pada batas
  negatif dapat mencapai 2,4 mA. [P01/P]

Keadaan aktual:
- Foto telah dimasukkan sebagai Gambar 4.6. [F04/F]
- Kecocokan model, pengaturan, sambungan, dan kalibrasi unit terpasang
  belum diverifikasi dari catatan pemasangan. [V]

### 5.5 Sensor aliran

Model pada naskah: SMC PFMB7202-06-C. [F02/D,F]

Spesifikasi model:
- Rentang ukur nominal 20–2000 L/min.
- Kode C menyediakan keluaran sakelar NPN dan keluaran analog 1–5 VDC.
- Karakteristik acuan: 1 V pada 0 L/min, sekitar 1,04 V pada 20 L/min,
  dan 5 V pada 2000 L/min. [P02/P]

Keadaan aktual:
- Foto telah dimasukkan sebagai Gambar 4.7. [F04/F]
- Model, label, pengaturan keluaran, kondisi referensi aliran,
  dan kalibrasi unit terpasang masih perlu dicocokkan. [V]

Titik acuan nol tidak sama dengan batas bawah rentang ukur nominal.
Laju aliran, volume akumulasi, dan ringkasan per siklus adalah besaran berbeda.

### 5.6 Waveshare dan perangkat alarm

- Modul masukan analog:
  Waveshare Modbus RTU Analog Input 8CH. [U08 + F02/U,F]
- Slave ID modul: 2. [U08/U]
- Keluaran transduser 4–20 mA dan 0–5 V dapat dibaca sesuai
  konfigurasi kanal. [U06/U; P04 untuk pemeriksaan kemampuan model]
- Sistem menggunakan satu adapter USB-to-RS485 untuk RTD Converter
  dan Waveshare Modbus RTU Analog Input 8CH yang terhubung paralel
  pada satu bus RS485. [U07 + U08 + U11/U]
- RFID, GPIO, relay, dan buzzer 24 VDC tercantum dalam naskah.
  [F02 + D01/D,F]
- Pembaca RFID, modul relay, dan buzzer dibahas dalam tiga sub-subbab
  terpisah sesuai persetujuan pengguna. Gambar 4.11 memuat pembaca RFID
  (images (11).jpg), Gambar 4.12 memuat foto modul relay dari pengguna
  (images (12).jpg; aset assets/gambar/gambar-relay.jpg), dan Gambar 4.13
  memuat buzzer (images (13).jpg). Foto relay ditambahkan pada
  19 November 2026. Keberadaan foto tidak memverifikasi konfigurasi
  pengawatan atau unit terpasang. [pengguna + F02 + F04/U,F]
- Setelah pemisahan, diagram dashboard menjadi Gambar 4.14; dokumentasi
  implementasi, HMI, dan dashboard menjadi Gambar 4.15?4.18. Label dan
  path aset sebelumnya dipertahankan agar referensi tidak rusak. [F02/F]

Belum terkonfirmasi:
- Pemetaan kanal, jumper, mode/rentang masukan, dan register Waveshare.
- Model RFID, relay, polaritas kendali, dan pengawatan alarm.
Status: V.

## 6. Arsitektur komunikasi RS485 cutting terkonfirmasi

Konfigurasi aktual:
- Sistem menggunakan tepat satu adapter USB-to-RS485.
- Adapter menghubungkan dua perangkat secara paralel pada satu bus RS485.
- Perangkat pertama: RTD Converter, Slave ID 1.
- Perangkat kedua: Waveshare Modbus RTU Analog Input 8CH, Slave ID 2.
- Kedua perangkat berkomunikasi melalui adapter USB-to-RS485 yang sama.

Sumber/status: U07, U08, dan U11/U.
Topologi ini dikonfirmasi langsung oleh pengguna pada 19 November 2026.

Jumlah adapter, susunan satu bus bersama, dan Slave ID kedua perangkat
bukan lagi informasi yang memerlukan konfirmasi.

Detail pengawatan yang belum diberikan:
- sambungan terminal A/B pada masing-masing perangkat;
- penggunaan dan sambungan ground referensi;
- penggunaan, nilai, dan lokasi terminasi.

Status detail pengawatan tersebut: V.
Jangan mengisi detailnya berdasarkan asumsi atau diagram konseptual.

Catatan migrasi merupakan arsip historis. Jika isinya bertentangan dengan
konfigurasi di atas, gunakan konfirmasi pengguna ini sebagai sumber terbaru.

## 7. Rumus konversi dan kondisi penggunaannya

Rumus berikut adalah hubungan matematis bersyarat. Keberadaannya tidak
membuktikan bahwa kode, kalibrasi, dan perangkat aktual sudah sesuai.

### 7.1 Konversi linier umum

y = y_min + (x - x_min) × (y_max - y_min) / (x_max - x_min)

Kondisi:
- Hubungan keluaran dan besaran terukur linier pada rentang tersebut.
- Titik ujung diketahui dari label/manual/konfigurasi.
- x sudah berupa besaran listrik dalam satuan yang benar, bukan raw ADC.
- x_max berbeda dari x_min.
- Offset, faktor kalibrasi, dan batas validitas diperhitungkan terpisah.

Sumber/status: hubungan matematis; penerapannya pada unit proyek memerlukan
data titik ujung dan konfigurasi aktual. [V untuk penerapan yang belum lengkap]

### 7.2 Transduser 4–20 mA

I_fasa = (I_out - 4) × I_maks / 16

Kondisi:
- 4 mA mewakili 0 A dan 20 mA mewakili I_maks.
- I_out dalam mA; I_fasa dan I_maks dalam A.
- I_maks berasal dari unit yang digunakan.
- Berlaku pada rentang linier yang ditentukan; bukan aturan untuk
  menafsirkan seluruh nilai gangguan atau di luar rentang.

Untuk unit pada foto, I_maks tercantum 20 A. [F04/F]
Kesesuaian unit terpasang dan kode masih perlu diverifikasi. [V]

### 7.3 Transduser 0–5 V

I_fasa = V_out × I_maks / 5

Kondisi:
- 0 V mewakili 0 A dan 5 V mewakili I_maks.
- V_out dalam volt; I_fasa dan I_maks dalam A.
- Hubungan linier dan titik ujung harus dikonfirmasi untuk varian aktual.

Jenis keluaran 0–5 V dikonfirmasi pengguna. [U06/U]
Batas ukur dan pemetaan titik ujung unit aktual belum dikonfirmasi. [V]
Jangan mengisi I_maks = 20 A secara otomatis.

### 7.4 Tekanan ISE30A-01-D

P_MPa = (I_out_mA - 4) / 16

Kondisi:
- Menggunakan karakteristik nominal 4 mA pada 0 MPa dan 20 mA pada 1 MPa.
- Tidak ada perubahan skala/offset yang membuat titik ujung berbeda.
- Kanal menghasilkan nilai arus mA yang benar.
- Penggunaan rentang negatif mengikuti batas dan karakteristik manual.

Sumber: P01/P. Kesesuaian pengaturan unit proyek: V.

### 7.5 Aliran PFMB7202-06-C

Q_Lmin = (V_out - 1) × 500

Kondisi:
- Menggunakan karakteristik nominal 1 V pada 0 L/min dan 5 V pada
  2000 L/min.
- Skala keluaran analog tidak diubah dari karakteristik tersebut.
- V_out dalam volt.
- Batas rentang ukur nominal 20–2000 L/min tetap diperhatikan.
- Jangan menyatakan akurasi di bawah batas nominal dari rumus ini saja.

Sumber: P02/P. Kesesuaian pengaturan unit proyek: V.

### 7.6 Suhu

Jangan mengonversi register suhu dengan rumus atau faktor skala perkiraan.
Gunakan manual konverter dan kode aktual. Karakteristik PT100 tidak boleh
dianggap linier sempurna untuk seluruh rentang.

Sumber: P03 untuk karakteristik dasar; register konverter proyek: V.

## 8. Arsitektur dan perangkat lunak cutting yang tercatat

Arsitektur komunikasi terkonfirmasi:
- RTD Converter menggunakan Slave ID 1.
- Waveshare Modbus RTU Analog Input 8CH menggunakan Slave ID 2.
- Kedua perangkat terhubung secara paralel pada satu bus RS485.
- Bus tersebut terhubung melalui satu adapter USB-to-RS485 yang sama.

Sumber/status: U07, U08, dan U11/U.

Alur pengukuran dan penyajian dalam naskah:
- PT100 → RTD Converter.
- Transduser arus, sensor tekanan, dan sensor aliran →
  Waveshare Modbus RTU Analog Input 8CH.
- Bus RS485 → satu adapter USB-to-RS485 → Raspberry Pi 5.
- Raspberry Pi → HMI, histori, dan alarm.
- Telemetri → MQTT → dashboard.

Sumber/status alur pengukuran dan aplikasi: F02 + D01/D,F.
Raspberry Pi 5 sebagai komputer utama: U12/U.
Konfigurasi bus dan adapter mengikuti konfirmasi pengguna di atas.
Detail terminal A/B, ground referensi, dan terminasi tetap berstatus V.

Naskah dashboard mencantumkan PC mesin, broker lokal, dan server.
Lokasi broker, jalur komunikasi jaringan, dan deployment aktual belum
diverifikasi.
Sumber/status: F02 + D01/D,V.

Perangkat lunak yang disebut:
Python, PyQt5, pyqtgraph, minimalmodbus, pyserial, SQLite, paho-mqtt,
Django, HTML, CSS, JavaScript, dan Chart.js.
Sumber/status: F02 + D01/D,F.

Interval tiga detik, rata-rata 60 detik, logika alarm, FlowCycles,
antrean, dan ACK berasal dari uraian draft.
Ambang siklus 5 dan 2 L/min berada di bawah rentang nominal sensor 20 L/min;
penerapannya sebagai deteksi siklus memerlukan verifikasi. Waktu konfirmasi
1 detik tidak menjamin respons 1 detik pada sampling nominal 3 detik.
Sumber/status: D01 + F02/D,V; P02/P untuk batas sensor.

Klaim penerapan pada kedua mesin dan penerimaan pembimbing tercantum
dalam naskah. Bukti pengujian/penerimaan belum diperiksa.
Sumber/status: D01 + F02/D,V.

## 9. Sistematika dan status pekerjaan

- Bab I — Pendahuluan:
  naskah mencakup cutting dan panel; lingkup panel diselaraskan dengan kode serta konfirmasi operasional.
- Bab II — Gambaran Umum Perusahaan:
  naskah tersedia; Gambar 2.1–2.25 terisi.
- Bab III — Landasan Teori:
  naskah tersedia; perlu sinkronisasi dengan implementasi final.
- Bab IV — Rancangan dan Implementasi Sistem:
  pembahasan panel dan kontribusi Fadhil ditambahkan; dokumentasi pemasangan serta pengujian terukur masih perlu dilengkapi.
- Bab V — Penutup:
  naskah tersedia; kesimpulan harus mengikuti hasil final.
- Halaman awal:
  tersusun; tanggal pengesahan/kata pengantar belum lengkap.
- Lampiran:
  struktur 16 lampiran tersedia; dokumentasi dan biodata belum lengkap.

Sumber/status: F01–F04/F.
“Naskah tersedia” bukan persetujuan final pembimbing.

Pekerjaan terbuka:
- Gambar 4.13–4.16; foto relay untuk melengkapi Gambar 4.11.
- Dua belas gambar Lampiran 1–12.
- Logbook bertanggal/paraf Lampiran 13–14.
- Pasfoto, biodata, kegiatan, dan penghargaan penulis.
- Tanggal pengesahan dan kata pengantar.
- Foto, pengawatan, konfigurasi node terpasang, dan rekaman pengujian panel. Model panel sudah dikonfirmasi Raspberry Pi 5 pada U19.
- Bukti pengujian, kode, dan penerimaan.
- Detail pengawatan RS485: terminal A/B, ground referensi, dan terminasi.
- Konfigurasi perangkat lain yang masih berstatus V.
- Peninjauan metadata pustaka, tahun terbit, dan tanggal akses.
- Pemeriksaan keterbacaan diagram dan peringatan kompilasi mengikuti hasil build terbaru.

Sumber/status: F01–F07/F,V sesuai jenis kekurangannya.

## 10. Konfigurasi LaTeX dan build

Konfigurasi aktif:
- report, 10pt, a5paper, twoside, openright, fleqn.
- A5: 148 × 210 mm.
- Margin dalam 2,5 cm; luar 2 cm; atas 2,5 cm; bawah 2 cm.
- Isi utama single spacing.
- secnumdepth dan tocdepth 3.
- Caption gambar rata tengah.
- natbib, BibTeX, apalike.
- longtblr/tabularray untuk tabel utama.

Sumber/status: F05/F.

Toolchain:
- .latexmkrc mengatur pdflatex dan keluaran/auxiliary di build/.
- Makefile target buku memanggil latexmk -pdf main_buku.tex.
- Makefile juga memakai utilitas bergaya POSIX dan menyalin PDF ke
  output/ dengan nama bertanggal.
- TinyTeX ditemukan di:
  C:/Users/mfand/AppData/Roaming/TinyTeX/bin/windows/
- Konfigurasi LaTeX Workshop tersedia pada proyek dan User Settings.

Sumber/status: F05 dan pemeriksaan lokasi executable/F.
Ketersediaan PATH, make, utilitas shell, dan perilaku lingkungan harus
diperiksa kembali sebelum kompilasi. Jangan menganggapnya universal.

Dokumen utama: main_buku.tex.
PDF build: build/main_buku.pdf.
PDF yang selama ini dibagikan:
output/Laporan_KP_Fandy_Fadhil_Migrasi_LaTeX.pdf.

## 11. Baseline audit

Pada 19 November 2026:
- PDF 104 halaman.
- 41 label gambar, 3 tabel utama, 16 lampiran.
- 11 entri pustaka.
- 17 kotak Ruang gambar.
- PDF build dan output identik berdasarkan hash.
- Tidak ada sumber/aset lebih baru daripada PDF.
- Log terakhir tidak menunjukkan error, Overfull, label ganda,
  atau rujukan/sitasi tidak terselesaikan.
- Terdapat pesan Underfull, substitusi font label HMI,
  dan pengaturan caption tabel yang tidak digunakan.
- Audit tidak menjalankan kompilasi ulang.

Sumber/status: F07/F. Angka ini harus dihitung ulang setelah perubahan.

Folder tidak memiliki metadata Git. [audit/F]
Backup tersedia menurut pengguna. [U10/U]

## 12. Sumber historis dan referensi

H01 menyimpan jejak migrasi, bukan keadaan terbaru.
CATATAN_MIGRASI.md masih memuat jumlah halaman, referensi, dan uraian
komunikasi yang sudah tertinggal. Gunakan berkas aktual serta konfirmasi
pengguna terbaru untuk menentukan keadaan proyek.

Citation key yang tersedia pada baseline:
modbus2012, raspberrypi, touchdisplay, pyqt, sqlite, mqtt2014,
django, waveshare, smcise30a, smcpfmb, pt100reference. [F06/F]

Referensi yang ditolak pengguna:
- karya internal Anggriawan 2026a dan 2026b yang sebelumnya dimasukkan;
- laporan Arifin dan Yusuf 2026.
Jangan memasukkannya kembali tanpa perubahan instruksi pengguna. [U09/U]

## 13. Pemeliharaan konteks

Saat penulisan berkas diizinkan, setiap pembaruan mencatat:
informasi, sumber, status, lokasi terkait, dan tanggal bila tersedia.

Pertahankan konflik yang belum terselesaikan. Ubah status hanya berdasarkan
bukti baru. Jangan menganggap pengulangan klaim dalam bab, tabel, dan
diagram sebagai beberapa bukti independen.

## 14. Perbaikan setelah audit menyeluruh (19 November 2026)

Pengguna mengizinkan perbaikan temuan proporsionalitas tata letak, penulisan,
dan penyusunan. [U; instruksi percakapan terbaru]

Perubahan berkas:
- Kata pengantar dan etika dipadatkan tanpa menghilangkan pihak yang disebut
  atau prinsip utama; pengulangan tujuan/manfaat dikurangi. [F02/F03/F]
- Bab III dipadatkan untuk menghindari paragraf penutup pada halaman tersendiri.
- Diagram 4.1 disajikan sebagai vektor tegak dengan topologi yang sama;
  aset raster pengguna tetap disimpan. Detail pengawatan tidak ditambahkan.
- Foto perangkat diatur melalui LaTeX; berkas gambar asli dipertahankan.
- Ringkasan evaluasi dibedakan dari bukti uji terukur dan penerimaan.
- Kontribusi panel Fadhil dicatat sebatas konfirmasi pengguna.
- Metadata author PDF memuat kedua penulis. [F05/F]
- Tahun pada lima halaman web tanpa tanggal terbit eksplisit dicatat t.t.;
  tahun publikasi halaman Waveshare yang belum terverifikasi juga dicatat t.t.
  Akses ulang ke wiki Waveshare ditolak HTTP 403; ini bukan verifikasi baru
  spesifikasi atau tanggal publikasinya.
  Tanggal akses historis dipertahankan. Judul manual OMEGA disesuaikan dengan
  halaman judul sumber resmi. [F06/F; sumber primer di URL masing-masing]

Perubahan penyajian bukan bukti baru bahwa konfigurasi, pengujian, atau
penerimaan lapangan telah diverifikasi. Pekerjaan terbuka pada bagian 9 dan
status V tetap berlaku.

### Penyesuaian korelasi mata kuliah (19 November 2026)

Sumber: tiga tangkapan layar daftar mata kuliah yang dikirim pengguna,
dengan penegasan bahwa daftar tersebut merupakan mata kuliah yang telah
ditempuh. [U; percakapan terbaru]

Bagian 4.3 disesuaikan dengan nama pada daftar: Pengukuran Listrik dan
Instrumentasi, Instrumentasi Elektronika, Rangkaian Listrik 1 dan 2,
Rangkaian Elektronika, Piranti Elektronika, Workshop Algoritma dan
Pemrograman, Workshop Pemrograman Lanjut, Workshop Sistem Mikroprosesor dan
Antar Muka, Workshop Mikrokontroler, Pengolahan Sinyal, K3L dan Standar
Internasional, serta praktikum terkait yang tampak pada daftar. [U,F]

Nama mata kuliah yang sebelumnya tidak sesuai daftar diganti. Uraian
korelasi merupakan pemetaan konsep terhadap kegiatan yang sudah tercatat
dalam Bab IV, bukan verifikasi silabus rinci, nilai akademik, hasil uji,
atau sertifikasi sistem. Kode mata kuliah tidak disalin karena beberapa
kode pada tangkapan layar muncul berulang untuk nama yang berbeda.

### Penyesuaian judul dengan IIoT (19 November 2026)

Pengguna meminta agar judul memuat IIoT. Judul pada config/variables.tex
menjadi: Perancangan dan Implementasi Sistem Monitoring Mesin Cutting dan
Panel Berbasis Industrial Internet of Things (IIoT) Menggunakan Raspberry Pi.
[Sumber: instruksi pengguna terbaru/U; nilai judul dalam berkas/F]

Cakupan mesin cutting, panel, dan penggunaan Raspberry Pi dipertahankan.
Istilah IIoT mengikuti pembahasan konektivitas pengukuran dan pemantauan
terpusat yang telah ada pada Bab III?IV; perubahan judul tidak menambah
klaim implementasi atau rincian panel yang belum tersedia.

## 15. Integrasi proyek monitoring panel Fadhil (19 November 2026)

### 15.1 Sumber dan batas kepastian

- U13: diagram pengguna menunjukkan rancangan beberapa blok/node, perangkat
  THM30MD dan meter Schneider, satu Raspberry Pi beserta RFID/buzzer/LED per
  node, lalu Ethernet melalui switch menuju dashboard server. [U]
- U14: pengguna menyatakan Elmon-WithOut-shinenjin adalah dashboard server
  dan rpi_panel_monitor adalah program Raspberry Pi untuk proyek Fadhil. [U]
- U15: pengguna mengonfirmasi konfigurasi yang sudah berjalan: satu Raspberry
  Pi untuk empat panel di area Power Room, antarmuka modul UART--RS485;
  rancangan satu unit monitoring per blok panel berdekatan. [U]
- C01: C:/Users/mfand/Downloads/Magang FIX/Magang FIX/rpi_panel_monitor.
  Program node dibaca statis, tidak dijalankan atau diubah. [F]
- C02: C:/Users/mfand/Downloads/Magang FIX/Magang FIX/Elmon-WithOut-shinenjin.
  Program server dibaca statis; SQLite dibaca mode read-only. [F]
- P06: Schneider Electric, EasyLogic PM2100 Series User Manual NHA2779002-12,
  edisi Februari 2026, citation key schneiderpm2100; URL pada references.bib.
  Manual mengelompokkan PM2120 sebagai EasyLogic PM2100, bukan pengesahan
  model/firmware unit terpasang. [P; diperiksa pada 19 November 2026]

Fakta dalam kode membuktikan implementasi berkas, bukan keberhasilan seluruh
fitur di lapangan. U15 merupakan konfirmasi operasional pengguna, bukan
pengukuran akurasi/latensi. Model panel pada penelaahan awal belum disebutkan; konfirmasi pengguna U19 kemudian menetapkan Raspberry Pi 5 untuk kedua proyek. Catatan awal ini telah diperbarui oleh konfirmasi tersebut.

### 15.2 Arsitektur, perangkat, dan konfigurasi

- Satu Raspberry Pi melayani empat panel di Power Room dengan modul UART,
  sesuai U15. Jangan menggantinya menjadi adapter USB atau mengklaim banyak
  node sudah dipasang. [U]
- Program menangani PM2120 dan THM30MD. PM2120 dibaca untuk tegangan LL/LN,
  arus R/S/T/netral/rata-rata, daya aktif per fasa/total, faktor daya per fasa,
  frekuensi, dan energi; THM30MD menghasilkan data digital suhu/kelembaban.
  [C01/modbus_reader.py:137?239/F]
- Serial bawaan /dev/ttyAMA0, pencarian port alternatif, 19200 baud, 8N1,
  timeout 0,35 s dan jeda 0,05 s. Ini konfigurasi kode, bukan verifikasi
  pengawatan atau port aktif unit terpasang. [C01/config.py:69?77;
  modbus_reader.py:36?108/F]
- FC03 + CRC16, float32 big-endian; energi uint64 dibagi 1000 (Wh ke kWh).
  Alamat yang dikirim sesuai offset -1: 2999/3019/3027/3035/3053/3077/3109/3203.
  THM30MD membaca alamat 2 sebanyak 4 register. Kesesuaian dengan firmware
  dan skala aktual harus diuji. [C01/config.py:93?108; modbus_reader.py/F,V]
- JSON node yang diserahkan hanya memuat panel 1 dengan pasangan slave 1/2.
  Database server memuat empat panel dengan pasangan 1/2, 3/4, 5/6, 7/8.
  Pemasangan empat panel dikonfirmasi U15, tetapi konfigurasi lengkap node
  terpasang belum diarsipkan dalam berkas yang dibaca. [C01/panels_config.json;
  C02/db.sqlite3 query read-only/F,V]
- device ID bawaan rpi-1; panel ID berbeda dari device ID dan slave ID.
  Panel.panel_id unik global pada server. [C01/config.py:21?42;
  C02/apps/panel_monitor/models.py:21?47/F]
- Pin BCM bawaan: buzzer 18 aktif HIGH, LED merah 16/hijau 24 aktif LOW,
  RFID D0/D1 pada 20/21. Pembaca Wiegand 26/32 bit, backend prioritas lgpio,
  alternatif RPi.GPIO, gpiozero, lalu mock. Ketersediaan mock bukan bukti
  GPIO fisik bekerja. [C01/config.py; alarm_actuator.py; rfid_reader.py/F]
- Sumber belum memastikan terminal A/B, ground, terminasi, antarmuka listrik,
  skema driver, model reader/aktuator, rasio CT, atau firmware meter. [V]

### 15.3 Siklus data dan dashboard

- Polling seluruh panel dan publikasi bawaan tiap 300 s. Alarm lokal
  dievaluasi ketika pembacaan dilakukan. Pengolahan lokal tidak berarti
  pemantauan kontinu atau respons nol milidetik. [C01/main.py:139?160,383?450/F]
- MQTT QoS1; topik panel/device/panel/data, rfid_ack, status dan cmd;
  LWT retained untuk offline. Node berlangganan topik perangkat dan all.
  [C01/main.py:65?86,165?285,351?443/F]
- JSON mempersistenkan daftar panel, threshold, whitelist, dan mute.
  Tidak ditemukan antrean persisten telemetri/pengiriman ulang offline
  pada alur node yang ditelaah. Fitur ACK histori cutting jangan dipindahkan
  menjadi klaim panel. [C01/main.py/F]
- Server Django, paho-mqtt, Chart.js dan aset vendor lokal; SQLite aktif
  pada .env yang diserahkan. Kode juga menyediakan backend alternatif.
  Isi kredensial/alamat internal tidak disalin ke laporan. [C02/requirements.txt;
  config/settings.py; .env hanya pengaturan nonrahasia yang diperiksa/F]
- Timestamp telemetri ditetapkan saat diterima server (WIB), bukan timestamp
  ukur asli dari node. Interval minimum histori 300 s; batas offline 900 s.
  [C02/services/mqtt_subscriber.py:365?530; config/settings.py/F]
- Dashboard refresh 5000 ms; detail panel 60000 ms, history refresh 300000 ms;
  refresh browser tidak mempercepat polling perangkat. [C02/static/panel_monitor/js/
  dashboard.js:13,451; panel_detail.js:44?45/F]
- Model: Panel, Measurement, PowerFactorSample, StatsDaily, Alarm, AlarmEvent,
  ExportHistory, RfidCard. Histori, statistik, alarm, pengelolaan panel,
  settings/RFID, ekspor XLSX/CSV, diagnostik tersedia melalui API dan UI.
  Keberadaan model tidak membuktikan seluruh jalur telah mengisi data.
  [C02/models.py; views.py; urls.py; templates; static JS/F]
- Konsumsi energi bulanan dihitung terhadap rekaman awal bulan atau
  initial_energy, dibatasi minimum nol. Statistik berisi min/max/waktu,
  rata-rata, dan proporsi sampel dalam batas; bukan prediksi kerusakan.
  [C02/views.py:88?206,1154?1457; stats_service.py/F]
- Retensi bawaan: Measurement/PF 30 hari, StatsDaily 365 hari; Alarm inaktif
  >30 hari, tambahan seluruh Alarm >60 hari pada layanan cleanup.
  Ekspor dibatasi 10000 baris. [C02/services/stats_service.py:144?196;
  export_service.py:40?181/F]
- Layanan systemd mengatur autostart/restart proses, tetapi tidak dijalankan
  dalam penelaahan ini. Skrip diagnostik bukan log hasil lulus pengujian.
  [C01/panel-monitor.service; test_*.py; scan_modbus.py/F]

### 15.4 Temuan integrasi yang tidak boleh disembunyikan sebagai hasil lulus

1. MAYOR ? C01/modbus_reader.py:263?276 menghasilkan voltage_unbal_rs/st/tr/
   rn/sn/tn, sementara alarm_eval.py:160?166 memeriksa voltage_unbal,
   voltage_unbal_ll, voltage_unbal_ln. Alarm tegangan unbalance belum dapat
   dianggap tervalidasi; samakan kontrak data dan uji skenario. [F]
2. MAYOR ? C02/mqtt_subscriber.py:695?793 menghitung is_registered tetapi
   tidak menolak kartu sebelum ack dan memiliki fallback alarm lintas panel;
   node main.py:334?339 tetap melaporkan kartu ditolak. Perlu validasi yang
   konsisten pada server serta batas node/panel. [F]
3. MAYOR ? C02/mqtt_subscriber.py:598?692 memakai RfidCard pada baris 681
   tanpa impor pada fungsi/modul terkait. Jalur silenced+card_id berpotensi
   berhenti pada exception sebelum penyimpanan. Tambahkan impor pada proyek
   sumber jika kelak pengguna meminta perbaikan program, lalu uji jalurnya. [F]
4. MAYOR untuk perluasan ? publish_panel_command menerbitkan topik perangkat
   dan all (C02:856?859); seluruh node menerima broadcast (C01:175?178),
   handler tidak membatasi semua aksi berdasarkan target device. Dengan banyak
   node perintah dapat meluas. Verifikasi isolasi sebelum ekspansi. [F]
5. MAYOR ? nilai default nol/frekuensi 50 pada kegagalan blok parsial dan
   NaN/Inf menjadi nol tidak sama dengan hasil ukur valid; pm2120_ok tidak
   menjamin seluruh blok sukses. Server memiliki fallback arus S=(R+T)/2
   ketika data S hilang; jangan menyajikannya sebagai hasil ukur fasa S.
   [C01/modbus_reader.py:114?223; C02/services/mqtt_subscriber.py:517?524/F]
6. MAYOR ? evaluator node menerima PF negatif sebagai leading dan nilai >1
   sebagai 2-raw, sedangkan server hanya menerima raw 0..2. Ambang leading
   JSON node 0,90 vs default server pf_config 0,95; field delay PF server
   tidak dikirim/diterapkan sebagai timer evaluator node. Representasi meter
   dan ambang perlu diselaraskan; jangan klaim semua PF sudah tervalidasi.
   [C01/alarm_eval.py:176?208; C02/services/power_factor.py:33?46,
   pf_config.py; mqtt_subscriber.py:903?929/F; P06/P untuk konvensi tanda]
7. Kekurangan bukti ? snapshot SQLite yang diserahkan berisi 4 panel,
   0 Measurement/Alarm/StatsDaily/PowerFactorSample/RfidCard. Ini bukan bukti
   kegagalan pemasangan yang sudah dikonfirmasi U15; rekaman runtime terpisah
   masih diperlukan untuk evaluasi kuantitatif. [query mode read-only/F,V]
8. Batas ketahanan data ? QoS1 tidak menggantikan penyimpanan offline;
   sampel ketika mqtt_connected false tidak diarsipkan untuk kirim ulang.
   Perlu uji putus jaringan dan antrean jika kontinuitas histori disyaratkan.
   [C01/main.py:440?443/F]

Penelaahan memakai pembacaan statis dan AST seluruh 39 berkas Python,
pemetaan model/API/frontend serta pemeriksaan SQLite read-only; aplikasi,
MQTT, GPIO, perintah reset, deployment, dan skrip uji hardware tidak dijalankan.
Tidak ada perubahan pada kedua folder program sumber.

### 15.5 Penulisan laporan

Bab IV menambahkan pembahasan panel pada sec:monitoring-panel, satu diagram
vektor fig:panel-arsitektur berdasarkan diagram pengguna, empat tabel
parameter/register/batas/evaluasi, serta kontribusi Fadhil. Bab I, III, V,
abstrak, kata pengantar, dan sistematika diselaraskan. Struktur lima bab,
A5, margin bolak-balik, data dan gambar cutting dipertahankan.
Tidak dibuat hasil uji kuantitatif atau foto pemasangan rekaan. Judul tetap
mencakup cutting dan panel berbasis IIoT menggunakan Raspberry Pi.

Catatan penyajian integrasi: tautan manual Schneider, Django, standar MQTT, dan
Touch Display ditampilkan sebagai teks tautan deskriptif agar pustaka tidak
menyisakan satu entri pada halaman baru. URL tujuan lengkap dan metadata
referensi dipertahankan; font, spasi bibliografi, dan gaya apalike tidak diubah.

Validasi akhir integrasi panel:
- PDF 118 halaman, seluruhnya A5; 44 label gambar dan 12 referensi.
- Pembahasan panel 4.1.13 dimulai halaman tercetak 59; diagram 4.19 pada
  halaman 60; evaluasi tabel 4.6 pada halaman 68; kontribusi pada halaman 70.
- Foto relay tetap tersedia pada Gambar 4.12 halaman 52 setelah pergeseran.
- Kompilasi latexmk mengikuti .latexmkrc/TinyTeX, tanpa error, rujukan hilang,
  label ganda, atau Overfull. Pemeriksaan visual dilakukan pada bagian baru
  dan bagian yang terdampak. Underfull dan warning captionsetup tabel lama
  tetap dinilai sebagai peringatan tipografi; tidak dinyatakan build tanpa warning.
- Aset foto, main_buku.tex, config/, formats/, Bab II, dan kedua folder program
  sumber tidak diubah. Perbandingan memakai hash karena tidak ada metadata Git.

## 16. Ruang dokumentasi monitoring panel (20 November 2026)

Pengguna meminta ruang gambar agar kebutuhan dokumentasi panel terlihat
pada laporan. Empat belas placeholder ditambahkan dengan macro GambarLaporan
pada bagian 4.1.13, menggunakan caption rata tengah dan nama aset deskriptif.
Sumber/status: instruksi pengguna/U; chapters/bab4.tex/F.

Daftar kebutuhan (awalan aset assets/gambar/panel-):
- 01-unit.png ? Unit monitoring panel berbasis Raspberry Pi. Foto unit lengkap yang memperlihatkan Raspberry Pi, modul antarmuka, dan perangkat pendukung. [V: aset belum diberikan]
- 02-pm2120.png ? Meter Schneider Electric PM2120 pada panel listrik. Foto meter pada panel, dengan model dan tampilan pembacaan terbaca. [V: aset belum diberikan]
- 03-thm30md.png ? Sensor suhu dan kelembaban THM30MD pada panel. Foto sensor dan posisi pemasangannya di panel. [V: aset belum diberikan]
- 04-uart-rs485.png ? Pengawatan UART--RS485 pada node monitoring panel. Foto atau diagram pengawatan aktual dari Raspberry Pi melalui modul UART--RS485 ke perangkat panel. [V: aset belum diberikan]
- 05-rfid-alarm.png ? Pembaca RFID Wiegand, buzzer, dan indikator LED pada node panel. Foto perangkat RFID serta buzzer dan LED pada unit terpasang; beberapa foto boleh disusun menjadi satu gambar. [V: aset belum diberikan]
- 06-enroll.png ? Pendaftaran kartu RFID melalui dashboard panel. Tangkapan layar proses pendaftaran atau konfirmasi kartu pada dashboard; identitas pribadi disamarkan. [V: aset belum diberikan]
- 07-dashboard.png ? Halaman utama dashboard monitoring panel. Tangkapan layar ringkasan empat panel, status koneksi, dan parameter utama. [V: aset belum diberikan]
- 08-detail.png ? Halaman detail panel dan grafik parameter pengukuran. Tangkapan layar detail salah satu panel dengan nilai serta grafik yang terbaca. [V: aset belum diberikan]
- 09-history.png ? Halaman histori pengukuran panel berdasarkan rentang waktu. Tangkapan layar histori dengan pilihan panel, rentang waktu, dan rekaman yang tersedia. [V: aset belum diberikan]
- 10-alarms.png ? Halaman alarm dan status penanganan pada dashboard panel. Tangkapan layar alarm beserta status aktif dan acknowledgement sesuai kondisi yang benar-benar tersedia. [V: aset belum diberikan]
- 11-management.png ? Pengaturan identitas panel, slave ID, dan batas parameter. Tangkapan layar konfigurasi panel yang memperlihatkan pemetaan perangkat dan pengaturan batas; dapat terdiri atas beberapa tampilan. [V: aset belum diberikan]
- 12-statistics.png ? Ringkasan statistik dan analisis parameter panel. Tangkapan layar ringkasan atau analisis yang menunjukkan periode, minimum, maksimum, rata-rata, atau proporsi sampel dalam batas. [V: aset belum diberikan]
- 13-export.png ? Hasil ekspor data pengukuran panel dalam format XLSX atau CSV. Tangkapan layar contoh berkas ekspor yang sudah terbentuk, dengan judul kolom dan satuan terbaca. [V: aset belum diberikan]
- 14-power-room.png ? Pemasangan node monitoring untuk empat panel di Power Room. Foto kondisi aktual satu blok empat panel dan lokasi unit monitoring; dapat berupa gabungan foto area dan detail pemasangan. [V: aset belum diberikan]

Placeholder tidak merupakan bukti foto, tampilan, atau hasil uji yang telah
tersedia. Tidak dibuat foto atau tangkapan layar rekaan. Diagram arsitektur
panel sebelumnya serta seluruh gambar cutting dipertahankan. Nomor halaman
akan mengikuti hasil kompilasi terbaru; gunakan label gambar untuk rujukan.

Validasi ruang gambar: 14 label baru bernomor 4.20 sampai 4.33; total 30 ruang
gambar yang belum terisi di seluruh laporan. PDF terbaru 124 halaman A5.
Kompilasi berhasil tanpa error, label ganda, referensi hilang, atau Overfull.
Hanya bab4.tex dan konteks proyek yang disunting; aset foto dan template tetap.

## 17. Penyelarasan alur dengan laporan pembanding (20 November 2026)

Sumber U16: pengguna meminta alur isi mendekati laporan KP senior dan
secara eksplisit memilih "Tetap lima bab; samakan alur pembahasannya".
Status U: lima bab dipertahankan, termasuk Bab III Landasan Teori.
Laporan pembanding BUKU_KP_FIX_DIKUMPULKAN_2123600018.pdf hanya menjadi
acuan alur; identitas, perangkat, hasil, dan kontribusi proyek senior tidak
dipindahkan ke laporan ini. Struktur aktual pembanding empat bab berbeda
dari uraian sistematikanya; perbedaan tersebut tidak diikuti. [F]

Urutan Bab IV setelah penyelarasan: pengantar, observasi, kebutuhan, analisis
perangkat, alur dan pengembangan cutting, arsitektur, penyesuaian konfigurasi,
modul pendukung, pengembangan panel, integrasi dashboard, evaluasi cutting
dan panel, lalu dokumentasi pekerjaan. Kontribusi dan korelasi mata kuliah
tetap mengikuti bidang kegiatan. Evaluasi panel dipindahkan dari akhir
uraian pengembangan ke bagian pengujian, dengan seluruh batas bukti dan
ruang gambar tetap dipertahankan. [chapters/bab4.tex/F]

Keempat belas ruang gambar panel beserta label dan nama aset tetap tersedia.
Nomor gambar, tabel, subbab, dan halaman mengikuti kompilasi terbaru;
nomor pada catatan bagian 15 dan 16 merupakan keadaan sebelum penataan ini.
Status operasional satu Raspberry Pi untuk empat panel Power Room melalui
UART--RS485 tetap U15; penataan narasi tidak menaikkan kepastian hasil uji.

Validasi penyelarasan: PDF tetap 124 halaman A5, 58 label gambar unik,
12 entri pustaka, dan 30 ruang gambar belum terisi (14 untuk panel).
Pembahasan panel menjadi 4.1.10 halaman 54; integrasi 4.1.11 halaman 68;
pengujian 4.1.12 halaman 70; dokumentasi laporan 4.1.13 halaman 74;
kontribusi 4.2 halaman 75; korelasi mata kuliah 4.3 halaman 76.
Kompilasi latexmk berhasil tanpa error, rujukan hilang, label ganda,
Overfull, atau float terlalu besar. Peringatan Underfull dan captionsetup
tabel lama tetap ada. Pemeriksaan visual mencakup daftar isi dan halaman
Bab IV yang berubah; tabel parameter panel dirapikan secara lokal agar
baris terakhir tidak terpisah sendiri ke halaman berikutnya.
Perubahan sumber terbatas pada chapters/bab4.tex, pages/sistematika_kp.tex,
dan konteks ini. Template, Bab I--III dan V, referensi, serta aset tetap.

## 18. Penyederhanaan gaya bahasa (20 November 2026)

Sumber U17: pengguna meminta audit gaya bahasa agar mudah dipahami pembaca
awam, kemudian mengizinkan revisi berdasarkan temuan tersebut. Penyuntingan
diterapkan pada paragraf terpilih Bab I--V, abstrak, dan sistematika.
Kalimat umum serta pengulangan dikurangi; penjelasan fungsi didahulukan
sebelum rincian program. Register, node, broker, ACK, cache, dan istilah
terkait dijelaskan dengan bahasa yang lebih langsung. Dua judul anak subbab
panel disederhanakan menjadi siklus pembacaan/penyimpanan pengaturan dan
pengiriman data/perintah melalui MQTT. [F]

Tabel, rumus, label, jalur aset, kunci sitasi, dan informasi angka teknis
dipertahankan. Tidak ada hasil uji atau konfigurasi terpasang baru yang
ditambahkan. Batas bukti pengujian cutting dan panel tetap dicantumkan.
Struktur lima bab, format A5 bolak-balik, konfigurasi LaTeX, dan aset tetap.

Validasi: latexmk mengikuti Makefile/.latexmkrc dan TinyTeX yang tersedia.
PDF 124 halaman A5, 58 label gambar unik, 12 entri pustaka, dan 30 ruang
gambar (14 untuk panel). Tidak ada error, rujukan hilang, label ganda,
Overfull, atau float terlalu besar. Underfull dan peringatan captionsetup
tabel tetap ada. Halaman terpilih yang terdampak telah diperiksa secara
visual, termasuk abstrak, narasi, tabel, diagram, dan penutup. Nomor halaman
pada catatan sebelumnya bersifat historis dan dapat bergeser. Perbandingan
perubahan memakai hash berkas, bukan Git.

## 19. Penggantian Gambar 4.1 (20 November 2026)

Pengguna meminta gambar blok diagram berfoto yang dikirim dipasang kembali
sebagai Gambar 4.1. Aset assets/gambar/gambar-4-01.png telah diperiksa visual
dan cocok dengan gambar pengguna. Bab IV kini menyisipkan aset tersebut
secara langsung, tanpa rotasi, pemotongan, atau penyuntingan isi gambar.
Caption serta label fig:draft-3-1 dipertahankan. Diagram vektor terdahulu
di assets/diagrams/monitoring.tex tetap tersimpan tetapi tidak lagi dipakai
untuk Gambar 4.1. Istilah yang tertanam pada gambar mengikuti gambar asli
pengguna; istilah narasi laporan tetap HMI. [instruksi pengguna/U; berkas/F]

Kompilasi berhasil: 122 halaman A5. Gambar 4.1 berada pada halaman tercetak
39 (urutan PDF 63), tegak dan caption rata tengah. Halaman sebelum/sesudahnya
diperiksa visual. Tidak ada error, rujukan hilang, label ganda, Overfull,
atau float terlalu besar; peringatan tipografi sebelumnya tetap ada.
Perubahan sumber terbatas pada bab4.tex dan konteks ini; aset tetap utuh.

## 20. Penyiapan narasi untuk pengumpulan (20 November 2026)

Sumber U18: pengguna meminta naskah berorientasi laporan yang dikumpulkan
ke dosen, bukan catatan proses penyusunan. Kalimat pada abstrak tentang
konfirmasi pelaksanaan, kekurangan bukti, dan pemeriksaan program diganti
dengan ringkasan pekerjaan serta penerapan satu Raspberry Pi untuk empat
panel. Catatan penyusunan serupa pada Bab I, IV, V dan lampiran dirapikan.
Tanggal kata pengantar dikosongkan sesuai jawaban pengguna; tidak ditentukan
secara otomatis. [U/F]

Cakupan evaluasi tetap dinyatakan: penerapan, alur aplikasi, dan fungsi
monitoring; tidak ditambahkan angka akurasi, latensi, ketahanan, atau hasil
uji baru. Tabel tab:panel-evaluasi diubah menjadi cakupan evaluasi, dengan
pemisahan dasar penerapan perangkat dan analisis program. Catatan keadaan
berkas sumber/snapshot basis data tetap tersimpan pada bagian 15 konteks ini,
bukan dianggap sebagai bukti kondisi operasional panel. Temuan teknis
pengalamatan broadcast, nama data ketidakseimbangan, nilai pengganti,
penanganan RFID, faktor daya, dan ketiadaan antrean panel tetap dijelaskan
pada evaluasi serta saran; tidak dianggap sudah diperbaiki pada kode.

Validasi: PDF 122 halaman A5, 58 label gambar unik, 12 entri pustaka.
Gambar 4.1 tetap menggunakan gambar pengguna pada halaman tercetak 39.
Kompilasi berhasil tanpa error, rujukan hilang, label ganda, Overfull, atau
float terlalu besar. Peringatan Underfull dan captionsetup tabel tetap ada.
Halaman terpilih yang berubah telah diperiksa visual. Konfigurasi template,
rumus, label, sitasi, serta aset gambar dipertahankan.

Kelengkapan pengumpulan tetap memerlukan 30 ruang gambar (14 panel), isi
logbook dan paraf, serta data/pasfoto biodata. Ruang yang telah diminta
pengguna tetap dipertahankan. Penghapusan kalimat editorial tidak berarti
kelengkapan itu sudah terisi. Tanggal penyusunan sengaja kosong atas U18.

## 21. Penamaan Raspberry Pi dan konfirmasi model panel (20 November 2026)

Sumber U19: pengguna mengonfirmasi bahwa monitoring mesin cutting dan panel
sama-sama memakai Raspberry Pi 5. Informasi ini menggantikan status model
panel yang sebelumnya belum terkonfirmasi; detail pengawatan, konfigurasi
node terpasang, dan hasil pengukuran tidak otomatis berubah kepastiannya.

Aturan naskah: gunakan Raspberry Pi pada narasi, tabel, judul bagian, caption,
dan teks diagram LaTeX aktif. Model Raspberry Pi 5 dijelaskan pada bagian
4.1.7.1 untuk kedua proyek. Judul sumber pustaka dan teks yang telah tertanam
pada gambar pengguna dipertahankan sesuai sumber/aset aslinya. [U/F]

Validasi penamaan: pada sumber naskah aktif, model disebut sekali pada
paragraf 4.1.7.1 (halaman tercetak 43), yang menjelaskan kedua proyek.
Caption Gambar 4.2, judul bagian, tabel komponen, dan diagram dashboard
menggunakan Raspberry Pi. Judul pustaka Raspberry Pi 5 tetap merupakan
judul sumber. Gambar raster pengguna tidak disunting. PDF 122 halaman A5,
kompilasi berhasil tanpa error, rujukan hilang, label ganda, atau Overfull;
halaman bagian perangkat dan diagram yang berubah diperiksa visual.

## 22. Modul RS485 monitoring panel: MAX3485 (20 November 2026)

Sumber U20: pengguna mengonfirmasi modul antarmuka RS485 monitoring panel
adalah MAX3485. Model modul ini kini berstatus U, menggantikan penyebutan
generik UART--RS485 sebagai nama perangkat. UART tetap merupakan antarmuka
data serial Raspberry Pi, sedangkan MAX3485 menangani pengiriman dan
penerimaan sinyal pada bus RS485; protokol perangkat tetap Modbus RTU.
Dokumentasi primer P07: Analog Devices, MAX3485 Product Information,
https://www.analog.com/en/products/max3485.html, diakses 20 November 2026.
Fungsi transceiver didukung P07; penggunaan modul pada unit terpasang
didasarkan pada U20, bukan disimpulkan dari spesifikasi pabrikan.

Naskah diperbarui pada abstrak, Bab I, III, IV, V, caption ruang pengawatan,
dan diagram panel. Path panel-04-uart-rs485.png serta label fig:panel-uart
tetap dipertahankan agar pengisian dokumentasi berikutnya tidak rusak.
Tidak ditetapkan pin UART, DE/RE, terminal A/B, ground referensi, terminasi,
atau fitur pengendalian arah otomatis karena rincian tersebut belum diberikan.
Satu adapter Waveshare USB--RS485 milik cutting tetap sesuai konfigurasi
sebelumnya; MAX3485 merupakan antarmuka proyek panel.

Validasi MAX3485: PDF 122 halaman A5, 58 label gambar unik, 13 entri
pustaka, dan 30 ruang gambar. Diagram panel, uraian komunikasi, caption
pengawatan, tabel kontribusi, serta pustaka diperiksa visual. URL rujukan
Waveshare ditautkan pada judul entri agar penambahan referensi MAX3485
tidak memisahkan satu baris pustaka ke halaman berikutnya; alamat lengkap
dan tanggal akses tetap dipertahankan. Kompilasi berhasil tanpa error,
rujukan hilang, label ganda, Overfull, atau float terlalu besar.

## 23. Subbab komponen perangkat keras panel (20 November 2026)

Sumber U21: pengguna meminta subbab komponen monitoring panel seperti
pembahasan komponen cutting. Bab IV kini memisahkan 4.1.10 rancangan panel,
4.1.11 Komponen Perangkat Keras Monitoring Panel, dan 4.1.12 Program dan
Komunikasi Sistem Monitoring Panel. Integrasi dashboard, evaluasi, dan
dokumentasi menjadi 4.1.13, 4.1.14, serta 4.1.15. Struktur lima bab dan
konfigurasi template tidak diubah. [U/F]

Komponen dijelaskan pada sembilan anak subbab: Raspberry Pi, PM2120,
THM30MD, MAX3485, pembaca RFID Wiegand, buzzer, LED, jaringan Ethernet dan
switch, serta komputer server. Uraian mengacu pada fakta pengguna, kode,
dan referensi yang telah tersedia. Switch tetap dijelaskan dalam rancangan
jaringan; tidak ditetapkan merek atau model unit terpasang. Tipe RFID,
tegangan buzzer/LED, catu daya panel, dan pin/pengawatan rinci tidak
ditambahkan tanpa konfirmasi. Pertanyaan spesifikasi sudah diajukan, tetapi
penyusunan komponen tidak bergantung pada perkiraan jawaban.

Ruang gambar unit, PM2120, THM30MD, serta gabungan RFID/buzzer/LED dipindahkan
ke komponen terkait, dengan path dan label lama tetap. Ditambahkan ruang
foto assets/gambar/panel-15-max3485.png, label fig:panel-max3485. Seluruh
14 ruang panel lama tetap tersedia. Label sec:raspberry-pi ditambahkan
untuk merujuk model kedua proyek di 4.1.7.1; penyebutan Raspberry Pi 5 tetap
hanya satu pada narasi. Tabel parameter/register/batas/evaluasi tetap utuh.

Validasi: PDF 128 halaman A5; subbab komponen dimulai halaman tercetak 55,
program panel halaman 59. Terdapat 59 label gambar unik, 13 entri pustaka,
dan 31 ruang gambar (15 panel). Kompilasi berhasil tanpa error, rujukan
hilang, label ganda, Overfull, atau float terlalu besar. Halaman komponen,
tabel, ruang gambar, dan daftar isi diperiksa visual. Underfull serta
peringatan captionsetup tabel sebelumnya tetap ada.

## 24. RFID panel terintegrasi dan adaptor 12 V (20 November 2026)

Sumber U22: pengguna menjelaskan bahwa RFID panel memakai keluaran D0/D1,
berbeda dari RFID USB milik cutting. Buzzer dan LED sudah terintegrasi
pada RFID reader; keduanya tidak disajikan sebagai perangkat fisik terpisah.
Pengguna juga mengonfirmasi penggunaan adaptor 12 V sebagai catu daya.
Merek/model reader, arus adaptor, level logika D0/D1, serta pembagian jalur
daya belum ditetapkan dari keterangan ini. Pertanyaan cakupan suplai adaptor
sudah diajukan; tidak diasumsikan adaptor langsung memasok Raspberry Pi,
MAX3485, atau pin sinyal. Informasi 12 V dicatat sebagai keluaran adaptor.

Subbab komponen digabung menjadi 4.1.11.5 Pembaca RFID Wiegand dengan Buzzer
dan LED Terintegrasi. Subbab 4.1.11.6 membahas Adaptor 12 V, diikuti jaringan
dan server pada 4.1.11.7--8. Ruang gambar fig:panel-rfid-alarm dan path lama
tetap digunakan untuk satu reader utuh. Ditambahkan ruang foto
assets/gambar/panel-16-adaptor-12v.png, label fig:panel-adaptor-12v.
Abstrak, Bab I, III, IV, V dan diagram panel diselaraskan. Pemetaan GPIO
bawaan pada kode tetap dicatat sebagai konfigurasi program, bukan bukti
pengawatan atau jumlah perangkat fisik. Ketentuan RFID/relay/buzzer pada
proyek cutting tidak diubah. [U/F]

Validasi: PDF 128 halaman A5, 60 label gambar unik, 13 entri pustaka, dan
32 ruang gambar (16 panel). Kompilasi berhasil tanpa error, rujukan hilang,
label ganda, Overfull, atau float terlalu besar. Diagram serta halaman
komponen dan tabel sekitar perubahan diperiksa visual. Peringatan Underfull
dan captionsetup tabel sebelumnya tetap ada. Template serta aset tetap.

## 25. Cakupan suplai adaptor 12 V panel (20 November 2026)

Sumber U23: pengguna menegaskan adaptor 12 V hanya memasok RFID reader.
Catu ini mencakup reader dengan buzzer dan LED bawaan sebagai satu perangkat,
bukan sumber suplai seluruh node. Cakupan suplai yang sebelumnya menunggu
klarifikasi kini terkonfirmasi. Tidak ditambahkan hubungan adaptor ke
Raspberry Pi, MAX3485, PM2120, atau THM30MD. Level logika D0/D1, arus
adaptor, dan rincian pin tetap mengikuti bukti pengawatan yang tersedia.

Uraian dan caption pada 4.1.11.6 serta diagram panel diperbarui agar
12 V jelas merujuk catu RFID reader. Path dan label gambar dipertahankan.

Validasi suplai RFID: PDF tetap 128 halaman A5. Kompilasi berhasil tanpa
error, rujukan hilang, label ganda, atau Overfull. Diagram dan halaman
adaptor diperiksa visual; gambar dan label lama dipertahankan.

## 26. Skematik dan PCB monitoring panel (20 November 2026)

Sumber U24: pengguna menampilkan dua gambar pada percakapan, berupa skematik
dan layout PCB monitoring panel. Gambar dapat dibaca secara visual, tetapi
berkas gambar belum ditemukan di workspace, Downloads, dan direktori lokal
yang relevan. Tidak dibuat gambar pengganti atau rekonstruksi rangkaian.
Disiapkan subbab Skematik dan Layout PCB Antarmuka Panel dengan path
assets/gambar/panel-17-skematik.png dan panel-18-pcb.png, label
fig:panel-skematik serta fig:panel-pcb. Penyisipan gambar aktual menunggu
berkas asli yang dapat diakses.

Pembacaan visual U24: skematik memuat blok POWER, RFID CONTROL, dan RS485;
modul penurun XL4015, regulator berlabel REG1117, jaringan resistor D0/D1,
transistor Q1/Q2 berlabel BC547, konektor RFID dan konektor komunikasi.
Uraian naskah dibatasi pada bagian yang terbaca, tanpa klaim nilai tegangan
aman, pengujian, atau pemetaan GPIO aktual.

Perlu klarifikasi: label daya skematik menunjukkan 24 V, keluaran 5 V/12 V,
dan regulator 3,3 V; U23 menyatakan adaptor 12 V khusus RFID. Perlu diketahui
apakah gambar merupakan rancangan atau susunan yang benar-benar dipasang.
Modul RS485 pada gambar berlabel XY-017; hubungan label modul tersebut
dengan IC MAX3485 yang dikonfirmasi U20 juga ditanyakan. Jangan mengubah
konfirmasi pemasangan sebelumnya berdasarkan dugaan dari gambar.

Validasi persiapan skematik/PCB: PDF 130 halaman A5, kompilasi berhasil
tanpa error, rujukan hilang, label ganda, atau Overfull. Halaman subbab
dan dua ruang gambar diperiksa visual. Kedua ruang masih placeholder,
bukan gambar pengguna yang sudah terpasang; penyisipan aktual belum selesai.

## 27. Konfirmasi skematik terpasang dan modul XY-017 (20 November 2026)

Sumber U25: pengguna mengonfirmasi bahwa skematik U24 menunjukkan catu daya
yang benar-benar terpasang dan modul XY-017 pada gambar berbasis MAX3485.
Uraian terpasang kini mengikuti masukan 24 V, dua modul XL4015 untuk jalur
5 V dan 12 V, serta regulator REG1117 untuk jalur 3,3 V dari 5 V. Jalur
12 V digunakan untuk RFID reader dengan buzzer dan LED bawaan. Rujukan
ke adaptor 12 V terpisah pada naskah diganti dengan rangkaian daya PCB.
Konfirmasi ini menggantikan tafsir sumber 12 V sebelumnya (U22--U23);
fakta bahwa RFID dicatu 12 V tetap dipertahankan. Status konflik daya
dan hubungan XY-017/MAX3485 pada bagian 26 kini terselesaikan. [U]

Tidak ditambahkan arus catu, rating sekring, jalur daya Raspberry Pi,
pemetaan GPIO aktual, ataupun level sinyal D0/D1 di luar yang dapat dibaca
dan dikonfirmasi. Nama REG1117 mengikuti label gambar; tidak dianggap
konfirmasi nomor varian pabrikan yang lebih spesifik.

Subbab komponen kini menyebut Modul XY-017 Berbasis MAX3485 serta Rangkaian
Catu Daya. Slot foto adaptor yang keliru diarahkan ulang menjadi
assets/gambar/panel-16-catu-daya.png; label fig:panel-adaptor-12v dipertahankan
untuk kompatibilitas rujukan. Tidak ada aset foto yang dihapus. Dua gambar
skematik/PCB tetap menunggu berkas asli yang dapat diakses dan belum
terpasang sebagai gambar aktual pada PDF.

Validasi konfirmasi skematik: PDF tetap 130 halaman A5. Kompilasi berhasil
tanpa error, rujukan hilang, label ganda, atau Overfull. Diagram, uraian
XY-017/MAX3485, serta rangkaian daya diperiksa visual. Gambar skematik dan
layout PCB masih berupa ruang gambar sampai file asli tersedia.

## 28. Penegasan sumber catu panel (20 November 2026)

Sumber U26: pengguna menegaskan power supply 24 V diturunkan melalui
step-down menjadi 12 V untuk keperluan RFID. Narasi rangkaian daya kini
menyebut sumber power supply 24 V secara eksplisit dan alur XL4015/MOD2
menuju RFID reader 12 V. Ini memperjelas U25, tanpa mengubah jalur 5 V
dan 3,3 V pada skematik yang sudah dikonfirmasi. Tidak ada adaptor 12 V
terpisah yang dinyatakan sebagai sumber terpasang.

Validasi U26: kompilasi berhasil tanpa error atau rujukan hilang;
halaman catu daya diperiksa visual dan PDF dibagikan diperbarui.

## 29. Pembatasan uraian catu daya panel (20 November 2026)

Sumber U27: pengguna meminta istilah MOD1/MOD2 tidak dipakai dan uraian
jalur 5 V serta regulator 3,3 V dihilangkan dari naskah. Bab IV kini
menjelaskan alur power supply 24 V ke step-down XL4015, lalu 12 V untuk
RFID reader. Uraian skematik diselaraskan agar informasi yang dihapus
tidak diulang di bagian lain. Ini merupakan pembatasan isi narasi, bukan
perubahan rangkaian fisik atau klaim bahwa komponen pada skematik dihapus.

## 30. Pembaruan diagram, gambar 4.15--4.20, dan suplai Raspberry Pi dari XL4015 (25 November 2026)

Sumber U28: pengguna memperbarui diagram arsitektur panel (`panel-monitoring.tex`)
dengan 4 unit PM2120 dan 4 unit THM30MD pada tiap node serta panah langsung dari
setiap Raspberry Pi menuju Switch Hub, menyisipkan dan menyesuaikan ukuran gambar
4.15--4.20 (`bab4.tex`), dan menegaskan bahwa suplai Raspberry Pi pada
monitoring panel berasal dari modul step-down XL4015 (jalur 5 V dari sumber 24 V).
Subbab 4.1.11.6 dan 4.1.11.7 pada `chapters/bab4.tex` diperbarui agar menyatakan
jalur 5 V ke Raspberry Pi dan jalur 12 V ke RFID reader dari modul step-down XL4015.

## 31. Konfirmasi pin GPIO UART modul MAX3485 (25 November 2026)

Sumber: `D:\esp32-firmware\rpi_panel_monitor\README.md`, `DEPLOYMENT_GUIDE.md`,
`config.py`, dan `modbus_reader.py` atas arahan pengguna (U29). Pada header 40-pin
Raspberry Pi 5 (`/dev/ttyAMA0`), modul MAX3485 terhubung ke Pin 8 (`GPIO 14` / TX)
dan Pin 10 (`GPIO 15` / RX), dengan catu daya `3,3 V` dari Pin 1 dan `GND` dari
Pin 6 (`PARITY_NONE` / None parity, 19200 bps, 8N1). Subbab 4.1.12.2 pada
`chapters/bab4.tex` telah diperbarui dan tanda `[ISI DETAIL]` terkait ditutup.

## 32. Kondisi observasi awal Power Room dan kendala kebijakan IT (25--26 November 2026)

Sumber U30: pengguna menjelaskan kondisi awal di Power Room bahwa kondisi
abnormal panel baru diketahui saat petugas melakukan patroli, serta kendala
kebijakan IT perusahaan yang tidak mengizinkan mikrokontroler terhubung
langsung ke switch hub dan tidak mengizinkan komunikasi perangkat lapangan ke
server melalui HTTP atau API, sehingga sistem menggunakan Raspberry Pi dan
protokol MQTT. Atas arahan pengguna pada 26 November 2026 (U31), Subbab 1.4.3
(`Metode Observasi`) di `chapters/bab1.tex` diringkas agar hanya menjelaskan
metode observasinya, sedangkan Subbab 1.4.2 (`Metode Wawancara dan Diskusi`)
ditambahkan keterangan diskusi harian dengan pembimbing lapangan dan
\textit{monthly report} tiap satu bulan sekali bersama manajer serta divisi terkait.
