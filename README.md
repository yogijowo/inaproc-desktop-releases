# INAPROC Desktop Exporter

Pusat Distribusi Resmi dan Berkas Instalasi Aplikasi Desktop INAPROC Exporter (Windows).

Aplikasi utilitas desktop berbasis Windows untuk mengekstraksi, memformat, dan mengekspor data pengadaan barang dan jasa pemerintah secara langsung dari Gateway API resmi INAPROC (LKPP) ke dalam berbagai format file: Microsoft Excel (.xlsx), CSV (.csv), JSON (.json), dan SQL Dump (.sql).

Dirancang khusus untuk mempermudah tugas pengelola LPSE, PPK, Pokja Pemilihan, Auditor Pengadaan, dan Analis Kebijakan di lingkungan Pemerintah Daerah, Kementerian, dan Lembaga Negara.

---

## Antarmuka Aplikasi

![Antarmuka Aplikasi INAPROC Exporter](image/image.png)

---

## Unduhan Rilis Resmi (Versi 0.1.1 Beta)

Berkas eksekusi resmi tersedia dalam dua varian paket untuk sistem operasi Windows (64-bit):

| Nama Berkas | Tipe Paket | Ukuran | Tautan Unduhan Langsung |
| :--- | :--- | :---: | :--- |
| **INAPROC.Exporter.Setup.0.1.1.exe** | Installer Wizard *(Direkomendasikan)* | 109.83 MB | [Unduh Installer](https://github.com/yogijowo/inaproc-desktop-releases/releases/download/v0.1.1/INAPROC.Exporter.Setup.0.1.1.exe) |
| **INAPROC.Exporter.0.1.1.exe** | Standalone Portable | 109.61 MB | [Unduh Portable](https://github.com/yogijowo/inaproc-desktop-releases/releases/download/v0.1.1/INAPROC.Exporter.0.1.1.exe) |

Catatan: Seluruh riwayat pembaruan dan metadata versi dapat dilihat melalui halaman [GitHub Releases](https://github.com/yogijowo/inaproc-desktop-releases/releases).

---

## Panduan Instalasi

### Metode 1: Menggunakan Installer Wizard (Rekomendasi)

Paket installer menyediakan integrasi penuh ke dalam sistem Windows, termasuk shortcut di Desktop dan Start Menu serta uninstaller resmi.

1. Unduh berkas `INAPROC.Exporter.Setup.0.1.1.exe` melalui tautan di atas.
2. Klik ganda berkas installer yang telah diunduh.
3. Apabila muncul peringatan keamanan **Windows SmartScreen** (*Windows protected your PC*):
   - Klik teks **More info** atau **Info selengkapnya**.
   - Klik tombol **Run anyway** atau **Tetap jalankan**.
   *(Peringatan ini wajar terjadi pada rilis aplikasi baru yang belum memiliki reputasi unduhan global dan belum berbayar sertifikat komersial)*.
4. Ikuti panduan wizard di layar untuk menentukan lokasi instalasi.
5. Setelah instalasi selesai, aplikasi siap dibuka melalui shortcut di Desktop atau Start Menu.

### Metode 2: Menggunakan Versi Portable

Versi portable dapat langsung dijalankan tanpa melalui proses instalasi dan tidak membutuhkan hak administrator.

1. Unduh berkas `INAPROC.Exporter.0.1.1.exe`.
2. Pindahkan berkas ke folder kerja pilihan Anda (misalnya di drive `D:\`, folder Dokumen, atau USB Flashdisk).
3. Klik ganda berkas untuk langsung membuka aplikasi.

---

## Panduan Konfigurasi Awal

Untuk alasan keamanan data instansi, aplikasi tidak memuat Kode KLPD maupun Token API bawaan di dalam program. Konfigurasi wajib diisi secara mandiri saat aplikasi pertama kali dijalankan:

1. Buka aplikasi **INAPROC Exporter**.
2. Pada layar utama, klik tombol **Pengaturan** di sudut kanan atas (atau klik tombol **Lengkapi Pengaturan** pada banner peringatan).
3. Isi kolom yang tersedia:
   - **Kode KLPD**: Masukkan kode instansi Anda (contoh: `D145` untuk Pemerintah Kabupaten Kudus).
   - **Nama Instansi / LPSE**: Masukkan nama instansi sebagai label tampilan wilayah Anda.
   - **Token API INAPROC**: Masukkan Bearer Token resmi yang diterbitkan oleh Direktorat Pengembangan Sistem Pengadaan Secara Elektronik - LKPP.
   - **URL Gateway**: Default menggunakan `https://data.inaproc.id`.
4. Klik tombol **Uji Koneksi Token** untuk memverifikasi apakah token Anda aktif dan dapat terhubung ke server INAPROC.
5. Jika verifikasi berhasil, klik **Simpan Pengaturan**.
6. Status indikator di panel atas akan berubah menjadi hijau (**Token Siap**), dan tombol ekspor akan terbuka.

---

## Panduan Ekspor Data

1. **Pilih Kategori**: Pada panel bilah sisi kiri, pilih kategori modul (Semua Aktif, Tender, RUP, E-Katalog, atau Archive).
2. **Pilih Endpoint API**: Klik pada kotak dropdown untuk mencari dan memilih nama laporan data pengadaan yang ingin ditarik.
3. **Tahun Anggaran**: Masukkan tahun anggaran laporan (misalnya: `2026`).
4. **Format Export**: Pilih format file keluaran yang dibutuhkan:
   - **Excel (.xlsx)**: Cocok untuk pengolahan spreadsheet dan analisis kantor.
   - **CSV (.csv)**: Cocok untuk pengolahan cepat dan import ke sistem lain.
   - **JSON (.json)**: Cocok untuk pengembangan perangkat lunak dan pertukaran data API.
   - **SQL Dump (.sql)**: Cocok untuk database administrator yang ingin langsung memasukkan data ke database.
5. **Mulai Proses**: Klik tombol **Export Data**.
6. **Unduh File**: Tunggu hingga proses pengambilan data selesai. Setelah log menampilkan status selesai, klik tombol **Unduh File**.

---

## Spesifikasi Format Ekspor

| Format File | Ekstensi | Karakteristik Teknis |
| :--- | :---: | :--- |
| **Microsoft Excel** | `.xlsx` | Dilengkapi perhitungan lebar kolom adaptif otomatis dan auto-filter pada baris header. Dibuat langsung di memori tanpa membebani disk. |
| **Comma-Separated Values** | `.csv` | Dilengkapi standar encoding UTF-8 Byte Order Mark (BOM) sehingga karakter khusus, gelar, dan teks bahasa Indonesia langsung terbuka rapi di Microsoft Excel. |
| **JavaScript Object Notation** | `.json` | Data terstruktur berformat rapi (*pretty-printed*) dengan indentasi standar dua spasi. |
| **SQL Script Dump** | `.sql` | Menghasilkan skrip DDL `CREATE TABLE IF NOT EXISTS` dan perintah `INSERT INTO` bertahap (batch 50 baris per query) yang kompatibel dengan MySQL, PostgreSQL, dan SQLite. |

---

## Cakupan Endpoint API

Aplikasi mendukung 64 endpoint Gateway INAPROC LKPP yang terbagi dalam modul-modul berikut:

### 1. Modul Tender (15 Endpoint Aktif)
- Jadwal Tahapan Non-Tender
- Jadwal Tahapan Tender
- Rekapitulasi eKontrak
- Daftar Pengumuman Tender
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

### 2. Modul RUP (9 Endpoint Aktif)
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

### 4. Modul E-Katalog Archive (5 Endpoint Aktif)
- Paket E-Purchasing Arsip
- Instansi dan Satuan Kerja Arsip
- Detail Komoditas Arsip
- Detail Penyedia Arsip
- Detail Distributor Arsip

### 5. Modul Dashboard (31 Endpoint - Dalam Pengembangan)
Modul dashboard statistik saat ini dinonaktifkan sementara karena masih dalam tahap pengujian integrasi gateway.

---

## Keamanan dan Privasi

- **Database Lokal**: Seluruh data pengaturan kredensial dan riwayat unduhan disimpan secara lokal pada komputer pengguna di direktori:
  `%APPDATA%\inaproc-exporter\inaproc_data.sqlite`
- **Zero Third-Party Telemetry**: Aplikasi tidak mengirimkan data pengguna, token, maupun isi laporan ke server pengembang maupun pihak ketiga lainnya. Seluruh lalu lintas data hanya berlangsung secara langsung antara komputer pengguna dan Gateway resmi LKPP (`https://data.inaproc.id`).
- **In-Memory Streaming**: Proses konversi data berlangsung di dalam memori kerja (RAM) komputer sehingga tidak meninggalkan berkas sampah sementara pada media penyimpanan.

---

## Persyaratan Sistem

- **Sistem Operasi**: Windows 10 (64-bit) atau Windows 11 (64-bit).
- **Prosesor**: Intel Core i3 / AMD Ryzen 3 atau yang setara.
- **Memori (RAM)**: Minimum 4 GB (Disarankan 8 GB untuk penarikan data dalam volume puluhan ribu baris).
- **Ruang Penyimpanan**: Minimal 300 MB ruang kosong pada hard disk atau SSD.
- **Koneksi Jaringan**: Akses internet aktif ke domain `data.inaproc.id`.
- **Kredensial**: Token API INAPROC resmi yang masih dalam masa berlaku.

---

## Informasi Pengembang

- **Nama Pengembang**: Yogi Anggoro (LPSE Kabupaten Kudus)
- **Profil GitHub**: [https://github.com/yogijowo](https://github.com/yogijowo)
- **Repositori Rilis Publik**: [https://github.com/yogijowo/inaproc-desktop-releases](https://github.com/yogijowo/inaproc-desktop-releases)

---

## Lisensi

Aplikasi ini didistribusikan di bawah ketentuan [MIT License](LICENSE). Hak Cipta (c) 2026 Yogi Anggoro.
