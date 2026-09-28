# INAPROC Exporter - Download Rilis Resmi

[![Release](https://img.shields.io/badge/Release-v0.1.1--Beta-d22b50?style=for-the-badge&logo=windows)](https://github.com/yogijowo/inaproc-desktop-releases/releases/latest)
[![Platform](https://img.shields.io/badge/Platform-Windows%2010%20%7C%2011%20(64--bit)-0078D6?style=for-the-badge&logo=windows)](https://github.com/yogijowo/inaproc-desktop-releases/releases/latest)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

Repositori publik ini adalah **pusat distribusi resmi dan unduhan aplikasi desktop INAPROC Exporter**. Repositori ini hanya menyediakan berkas instalasi (`.exe`) dan catatan rilis (*Changelog*).

---

## 📥 Download Aplikasi (Versi 0.1.1 Beta)

Silakan unduh versi terbaru pada halaman **[Releases](https://github.com/yogijowo/inaproc-desktop-releases/releases/latest)**:

| Paket File | Tipe | Keterangan |
| :--- | :---: | :--- |
| **`INAPROC Exporter Setup 0.1.1.exe`** | **Installer Wizard** *(Direkomendasikan)* | Termasuk shortcut Desktop, Start Menu, dan uninstaller. |
| **`INAPROC Exporter 0.1.1.exe`** | **Standalone Portable** | Langsung klik untuk menjalankan tanpa hak administrator. |

---

## ✨ Fitur Versi 0.1.1 (Beta)

* **Ekspor Multi-Format**:
  * **Excel (`.xlsx`)**: Dilengkapi auto-lebar kolom dan filter otomatis.
  * **CSV (`.csv`)**: Dilengkapi UTF-8 BOM, langsung terbaca rapi di Microsoft Excel.
  * **JSON (`.json`)**: Format data terstruktur siap integrasi API / database.
  * **SQL Dump (`.sql`)**: Skrip DDL `CREATE TABLE` dan batch `INSERT INTO` (MySQL / SQLite / PostgreSQL).
* **Keamanan Maksimal**:
  * Tanpa hardcoded token.
  * Token API dan profil KLPD disimpan di database lokal SQLite (`%APPDATA%`).
  * Sistem mengunci tombol ekspor otomatis jika konfigurasi belum lengkap.
* **Tampilan Native Ringan**:
  * Desain modern dengan palet warna Crimson Rose (`#d22b50`).
  * Paginasi otomatis limit 100 sesuai standar resmi Gateway INAPROC LKPP.
  * Dilengkapi 64 endpoint API (Tender, RUP, E-Katalog, Archive).

---

## 💻 Persyaratan Minimum Sistem
* **Sistem Operasi**: Windows 10 atau Windows 11 (64-bit).
* **Koneksi Internet**: Diperlukan untuk mengakses Gateway API INAPROC.
* **Otorisasi**: Memiliki Bearer Token resmi API INAPROC dari LKPP.

---

## 👨‍💻 Pengembang
* **Yogi Anggoro** (LPSE Kabupaten Kudus)
* **GitHub**: [@yogijowo](https://github.com/yogijowo)

---

## 🔒 Kebijakan Privasi
Aplikasi ini berjalan 100% di komputer pengguna secara lokal. Token API dan riwayat data unduhan tidak pernah dikirimkan ke server pengembang maupun pihak ketiga mana pun selain Gateway API resmi INAPROC LKPP (`https://data.inaproc.id`).
