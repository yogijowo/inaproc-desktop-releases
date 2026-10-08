# INAPROC Desktop Exporter

Pusat Distribusi Resmi dan Berkas Instalasi Aplikasi Desktop INAPROC Exporter (Windows).

Aplikasi utilitas desktop berbasis Windows yang ditenagai engine native Rust (Tauri v2) untuk mengekstraksi, memformat, menganalisis, mengaudit kepatuhan, dan mengekspor data pengadaan barang dan jasa pemerintah secara langsung dari Gateway API resmi INAPROC (LKPP) ke dalam berbagai format file: Microsoft Excel (.xlsx), CSV (.csv), JSON (.json), dan SQL Dump (.sql).

Dirancang khusus untuk mempermudah tugas pengelola LPSE, PPK, Pokja Pemilihan, Pejabat Pengadaan, Auditor Pengadaan, dan Analis Kebijakan di lingkungan Pemerintah Daerah, Kementerian, dan Lembaga Negara dengan performa tinggi dan konsumsi memori yang sangat efisien (< 50 MB RAM).

---

## Unduhan Rilis Resmi (Versi 1.0.0)

Berkas eksekusi resmi tersedia dalam dua varian paket untuk sistem operasi Windows (64-bit):

| Nama Berkas | Tipe Paket | Keterangan | Tautan Unduhan Langsung |
| :--- | :--- | :--- | :--- |
| **INAPROC.Exporter_1.0.0_x64-setup.exe** | Installer Wizard *(Direkomendasikan)* | Instalasi resmi dengan shortcut desktop & uninstaller | [Unduh Installer](https://github.com/yogijowo/inaproc-desktop-releases/releases/download/v1.0.0/INAPROC.Exporter_1.0.0_x64-setup.exe) |
| **INAPROC.Exporter_1.0.0_x64.msi** | Windows MSI Installer | Paket instalasi standar korporat Windows MSI | [Unduh MSI](https://github.com/yogijowo/inaproc-desktop-releases/releases/download/v1.0.0/INAPROC.Exporter_1.0.0_x64.msi) |
| **INAPROC.Exporter.exe** | Standalone Portable | Berkas portabel mandiri, langsung jalankan tanpa instalasi | [Unduh Portable](https://github.com/yogijowo/inaproc-desktop-releases/releases/download/v1.0.0/INAPROC.Exporter.exe) |

> Seluruh riwayat pembaruan dan rilis sebelumnya dapat dilihat melalui halaman [GitHub Releases](https://github.com/yogijowo/inaproc-desktop-releases/releases).

---

## Ringkasan Fitur Lengkap Versi 1.0.0

### 1. Dashboard Analitik & Statistik Real-Time
- **Analitik Perencanaan vs Realisasi**: Menyajikan metrik Belanja Pengadaan, Total RUP, Persentase Pengisian RUP, Komposisi Penyedia vs Swakelola, Produk Dalam Negeri (PDN), dan Usaha Mikro Kecil Koperasi (UMKK).
- **Tab Switcher Mode Analitik**: Beralih instan antara mode Berdasarkan Pagu (Nilai Rupiah) dan Berdasarkan Paket (Jumlah Kuantitas Paket).
- **Visualisasi Langsung**: Grafik Donut Chart, 100% Stacked Bar, dan Gauge Meter menampilkan nominal/kuantitas serta persentase secara langsung tanpa harus melakukan hover.
- **Tabel Peringkat Satker / OPD**: Pemantauan realisasi tiap Perangkat Daerah secara adaptif dengan fitur pencarian instan (live search) dan badge performa.

### 2. Modul Audit Kepatuhan & Deteksi Risiko PBJ
- **Mesin Audit Otomatis**: Memeriksa kepatuhan data paket RUP dan pengadaan terhadap ketentuan regulasi terbaru (Perpres 16/2018 jo 12/2021 jo 46/2025 serta Perlem LKPP 11/2021).
- **Pengaturan Ketentuan Sistem (CRUD Fleksibel)**: Pengguna dapat menambah, mengubah, mengaktifkan, atau menonaktifkan aturan batasan pengadaan (seperti ambang batas Pengadaan Langsung, Penunjukan Langsung, Swakelola, maupun ketentuan kustom instansi).
- **Deteksi Anomali & Risiko**: Identifikasi potensi pemecahan paket (anti-splitting Pasal 20), anomali HPS, dan potensi deviasi pemilihan penyedia.
- **Tampilan Spreadsheet Interaktif**: Antarmuka tabel bergaya spreadsheet lengkap dengan header kolom (A-K), formula bar, penanda status risiko (Kritis & Peringatan), serta ekspor laporan hasil audit ke Microsoft Excel (.xlsx).

### 3. Early Warning System Keterlambatan Tender
- **Komparasi RUP vs SPSE**: Menyandingkan target jadwal rencana pemilihan di RUP dengan paket tender yang sudah terbit di SPSE.
- **Peringatan Dini Keterlambatan**: Menandai paket yang telah melewati bulan rencana pemilihan namun belum ditenderkan untuk memitigasi risiko gagal lelang atau putus kontrak akhir tahun anggaran.
- **Bahan Evaluasi Pimpinan**: Memudahkan penyusunan bahan laporan rapat evaluasi pembangunan dan pengadaan (Tepra / Pimpinan Daerah).

### 4. Modul Statistik Moner (Monev SiRUP LKPP)
- **Monitoring & Evaluasi Per Program**: Rekapitulasi progres RUP per Program, Kegiatan, dan Satuan Kerja berbasis integrasi struktur Moner SiRUP.
- **Pemetaan Pagu & Keterisian**: Analisis Pagu Program, Pagu Pengadaan, Pagu Terumumkan, selisih anggaran, dan rasio ketercapaian.
- **Penyesuaian Pagu Tagging SiRUP**: Form input nilai Pagu Pengadaan Hasil Tagging SiRUP yang dilengkapi pemisah ribuan otomatis (titik) serta proteksi penyimpanan data lokal agar tidak hilang saat data dimuat ulang.
- **Pengelompokan Visual Rapi**: Pengelompokan data per OPD dengan header ringkasan yang jelas dan hasil ekspor Excel tabular siap olah.

### 5. Analisis Beban Kerja Personel Pengadaan (Workload Matrix)
- **Distribusi Penugasan**: Memetakan persebaran paket yang ditangani oleh Pokja Pemilihan maupun Pejabat Pengadaan.
- **Pengukuran Kapasitas Kerja**: Menganalisis jumlah paket aktif, akumulasi nilai pagu yang dikelola, dan status penyelesaian paket untuk pemerataan beban kerja organisasi pengadaan.

### 6. Asisten AI Pengadaan (Local RAG Copilot)
- **Integrasi Google Gemini AI (BYOK)**: Mendukung penggunaan API Key pribadi pengguna (model Gemini Flash) dengan akses kuota gratis harian.
- **Arsitektur Local RAG Efisien**: Mengambil konteks data relevan dari database lokal sebelum mengirimkan pertanyaan ke AI, menghemat konsumsi token hingga lebih dari 95% dan menghasilkan jawaban dalam hitungan detik.
- **Inspeksi 1-Klik**: Tombol analisis AI langsung dari baris tabel audit untuk memperoleh diagnosa risiko dan rekomendasi langkah tindak lanjut.

### 7. Ekspor Multi-Format Cepat (In-Memory Streaming)
- **Microsoft Excel (.xlsx)**: Pembuatan berkas langsung di memori dengan fitur auto-fit lebar kolom, format angka akuntansi, dan auto-filter.
- **Comma-Separated Values (.csv)**: Dilengkapi UTF-8 Byte Order Mark (BOM) sehingga karakter teks bahasa Indonesia langsung rapi saat dibuka di Microsoft Excel.
- **JavaScript Object Notation (.json)**: Struktur data rapi (pretty-printed) siap pakai untuk integrasi API dan sistem lain.
- **SQL Dump (.sql)**: Menghasilkan skrip DDL `CREATE TABLE IF NOT EXISTS` dan perintah `INSERT INTO` batch yang kompatibel dengan SQLite, MySQL, dan PostgreSQL.
- **Cakupan 33+ Endpoint API**: Mendukung seluruh endpoint resmi INAPROC (Tender, Non-Tender, e-Kontrak, RUP, E-Purchasing V6, Katalog, E-Katalog Arsip).

### 8. Sistem Pembaruan In-App (Auto-Updater)
- **Pemeriksaan Otomatis**: Mendeteksi rilis versi terbaru langsung dari repositori GitHub resmi.
- **Unduh Langsung di Aplikasi**: Tombol pembaruan langsung mengunduh berkas installer di dalam aplikasi lengkap dengan progress bar real-time.
- **Pemasangan Mandiri**: Installer otomatis dijalankan setelah proses unduh selesai untuk transisi versi yang mulus.

### 9. Keamanan, Privasi & Penyimpanan Lokal
- **Zero Third-Party Telemetry**: Aplikasi tidak mengirimkan token, konfigurasi, maupun isi laporan ke server pengembang atau pihak ketiga. Seluruh komunikasi data berlangsung langsung antara komputer pengguna dan Gateway resmi LKPP (`https://data.inaproc.id`).
- **Database Lokal SQLite**: Seluruh kredensial, cache analitik, riwayat ekspor, dan aturan kepatuhan tersimpan aman di penyimpanan lokal pengguna.
- **Native Rust HTTP Engine**: Menggunakan engine native Rust untuk koneksi HTTPS yang stabil tanpa kendala CORS.

### 10. Dukungan Apresiasi Pengembang
- Modal dukungan terintegrasi dengan opsi pembayaran standar nasional QRIS (dapat di-scan melalui aplikasi mobile banking atau e-wallet manapun) serta transfer saldo e-wallet (OVO, DANA, ShopeePay) dengan fitur salin nomor otomatis.

---

## Panduan Instalasi

### Metode 1: Menggunakan Installer Wizard (Rekomendasi)

Paket installer menyediakan integrasi penuh ke dalam sistem Windows, termasuk shortcut di Desktop dan Start Menu serta uninstaller resmi.

1. Unduh berkas `INAPROC.Exporter_1.0.0_x64-setup.exe` melalui tautan di atas.
2. Klik ganda berkas installer yang telah diunduh.
3. Apabila muncul notifikasi keamanan Windows SmartScreen:
   - Klik teks **More info** atau **Info selengkapnya**.
   - Klik tombol **Run anyway** atau **Tetap jalankan**.
   *(Pemberitahuan ini wajar pada berkas rilis open-source independen yang belum menggunakan sertifikat komersial berbayar tahunan)*.
4. Ikuti instruksi pada layar hingga proses instalasi selesai.
5. Aplikasi siap dibuka melalui shortcut di Desktop atau Start Menu.

### Metode 2: Menggunakan Versi Portable

Versi portable dapat langsung dijalankan tanpa melalui instalasi dan tidak membutuhkan hak administrator.

1. Unduh berkas `INAPROC.Exporter.exe`.
2. Letakkan pada folder kerja pilihan Anda (misalnya di drive `D:\`, folder Dokumen, atau flashdisk).
3. Klik ganda berkas untuk langsung membuka aplikasi.

---

## Panduan Konfigurasi Awal

Untuk menjaga keamanan kredensial instansi, aplikasi tidak memuat Kode KLPD maupun Token API bawaan. Konfigurasi diatur secara mandiri:

1. Buka aplikasi **INAPROC Exporter**.
2. Buka menu **Pengaturan** di bilah menu samping.
3. Isi data konfigurasi:
   - **Kode KLPD**: Kode instansi Anda (contoh: `D145` untuk Pemerintah Kabupaten Kudus).
   - **Nama Instansi**: Label instansi Anda (contoh: `Pemerintah Kabupaten Kudus`).
   - **Token Bearer INAPROC**: Token API resmi yang diterbitkan oleh LKPP.
   - **Tahun Anggaran Default**: Tahun anggaran default yang otomatis terisi pada formulir ekspor.
   - **Folder Penyimpanan**: Folder default tujuan penyimpanan file hasil ekspor.
4. Klik tombol **Uji Koneksi API** untuk memastikan token dan gateway dapat diakses.
5. Klik **Simpan Pengaturan**.

---

## Spesifikasi Format Ekspor

| Format File | Ekstensi | Karakteristik Teknis |
| :--- | :---: | :--- |
| **Microsoft Excel** | `.xlsx` | Auto-fit kolom dinamis, multi-sheet, format angka akuntansi, dan auto-filter header. |
| **Comma-Separated Values** | `.csv` | Standar encoding UTF-8 dengan Byte Order Mark (BOM) untuk kompatibilitas penuh dengan Excel. |
| **JavaScript Object Notation** | `.json` | Data terstruktur berformat rapi (pretty-printed 2 spasi) siap pakai untuk integrasi sistem. |
| **SQL Script Dump** | `.sql` | Menghasilkan skrip DDL `CREATE TABLE IF NOT EXISTS` dan perintah `INSERT INTO` batch yang kompatibel dengan SQLite, MySQL, dan PostgreSQL. |

---

## Cakupan Endpoint API INAPROC LKPP

Aplikasi mendukung endpoint Gateway INAPROC LKPP yang terbagi dalam modul-modul berikut:

### 1. Modul Tender & Non-Tender (15 Endpoint Aktif)
- Jadwal Tahapan Non-Tender
- Jadwal Tahapan Tender
- Rekapitulasi eKontrak
- Daftar Pengumuman Tender (dengan filter opsional kode tender)
- Pengumuman Non-Tender
- Rekapitulasi Non-Tender Selesai
- Pencatatan Non-Tender Realisasi
- Pencatatan Swakelola Realisasi
- Daftar Peserta Tender
- Peserta Tender Menang
- Tender Selesai Berdasarkan Nilai
- SPPBJ Tender
- Surat Pesanan E-Purchasing
- Realisasi E-Purchasing
- Rincian Paket Tender

### 2. Modul RUP / Rencana Umum Pengadaan (9 Endpoint Aktif)
- Master Satuan Kerja (Satker)
- Paket Anggaran Penyedia
- Paket Anggaran Swakelola
- Paket Penyedia Terumumkan
- Paket Swakelola Terumumkan
- Program Master RUP
- Daftar Paket Penyedia
- Daftar Paket Swakelola
- Riwayat Kaji Ulang RUP

### 3. Modul E-Katalog (4 Endpoint Aktif)
- Daftar Paket E-Purchasing Versi 6
- Detail Informasi Penyedia Katalog
- Daftar Produk Penyedia Katalog
- Daftar Kategori Produk Katalog

### 4. Modul E-Katalog Arsip (5 Endpoint Aktif)
- Paket E-Purchasing Arsip
- Instansi dan Satuan Kerja Arsip
- Detail Komoditas Arsip
- Detail Penyedia Arsip
- Detail Distributor Arsip

---

## Persyaratan Sistem

- **Sistem Operasi**: Windows 10 (64-bit) atau Windows 11 (64-bit).
- **Runtime**: Microsoft Edge WebView2 Evergreen Runtime (sudah tersedia secara bawaan di Windows 10 dan Windows 11).
- **Prosesor**: Intel / AMD 64-bit.
- **Memori (RAM)**: Minimal 2 GB (Disarankan 4 GB atau lebih).
- **Ruang Disk**: Minimal 50 MB ruang kosong.
- **Koneksi Jaringan**: Akses internet aktif ke `data.inaproc.id`.
- **Kredensial**: Token API INAPROC resmi yang aktif dari LKPP.

---

## Informasi Pengembang & Penafian (Disclaimer)

Aplikasi ini dikembangkan secara independen oleh:
- **Nama**: Yogi Anggoro, S.Kom
- **Jabatan**: Pranata Komputer Ahli Pertama pada Bagian Pengadaan Barang dan Jasa Sekretariat Daerah Kabupaten Kudus
- **GitHub**: [github.com/yogijowo](https://github.com/yogijowo)

**Penafian:**
Aplikasi ini bukan merupakan aplikasi resmi yang diterbitkan oleh Lembaga Kebijakan Pengadaan Barang/Jasa Pemerintah (LKPP) maupun GovTech Procurement / Telkom Indonesia. Aplikasi ini dibuat sebagai alat bantu utilitas mandiri bagi pengelola pengadaan di daerah untuk mempermudah backup, audit kepatuhan, analisis data, dan pelaporan.

---

## Lisensi

Aplikasi ini didistribusikan di bawah ketentuan [MIT License](LICENSE). Hak Cipta (c) 2026 Yogi Anggoro.
