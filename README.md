# Portal Berita Umbraco-React

Proyek ini adalah implementasi portal berita dinamis yang mengintegrasikan Umbraco CMS sebagai Backend REST API dan React sebagai Frontend.

## Versi Umbraco yang Digunakan
* Umbraco Version: Umbraco CMS versi 13.10.1

## Cara Menjalankan Project

### 1. Persiapan Backend (Umbraco)
- Buka file CompanyNewsPortal.sln di Visual Studio.
- Jalankan aplikasi (F5).
- API akan tersedia di: https://localhost:44362/api/news

### 2. Persiapan Frontend (React)
- Masuk ke folder 'client-app' melalui terminal.
- Jalankan 'npm install' untuk memasang library.
- Jalankan 'npm start' untuk memulai aplikasi di http://localhost:3000.

## Catatan Kendala dan Solusi
- Masalah Ambiguity (CS0229): Diselesaikan dengan merapikan struktur folder Controller agar tidak ada duplikasi servis.
- Sinkronisasi Data: Melakukan pemetaan ulang properti DTO (Title dan PublishDate) agar sesuai dengan kebutuhan Frontend.
- Navigasi: Mengintegrasikan link judul berita dari React untuk mengarah langsung ke halaman detail di Umbraco.
