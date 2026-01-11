# Company News Portal (Umbraco + React)

Proyek ini merupakan implementasi portal berita yang menghubungkan Umbraco CMS sebagai sumber data (Backend) dengan React.js sebagai antarmuka pengguna (Frontend).

Tujuan utama proyek ini adalah mendemonstrasikan bagaimana mengonsumsi konten dari CMS melalui REST API dan menyajikannya secara dinamis di sisi klien.

---

## Versi Umbraco yang Digunakan
* Umbraco Version: Umbraco CMS versi 13.10.1

---

## Cara Menjalankan Project

Silakan ikuti langkah-langkah di bawah ini untuk menjalankan aplikasi:

### 1. Persiapan Backend (ASP.NET Core / Umbraco)
1. Buka file solusi CompanyNewsPortal.sln menggunakan Visual Studio.
2. Jalankan aplikasi dengan menekan tombol F5 atau klik tombol Run.
3. API berita akan tersedia secara otomatis pada endpoint: https://localhost:44362/api/news.

### 2. Persiapan Frontend (React)
1. Buka terminal atau Command Prompt di dalam folder "client-app".
2. Instal semua dependensi dengan perintah: npm install.
3. Jalankan aplikasi React dengan perintah: npm start.
4. Aplikasi akan terbuka di browser pada alamat: http://localhost:3000.

---

## Catatan Kendala dan Solusi

Berikut adalah beberapa tantangan teknis yang berhasil diatasi selama proses pengembangan:

1. Konflik Definisi (Ambiguity Error CS0229):
   - Masalah: Terjadi bentrokan definisi _newsService karena adanya duplikasi Controller.
   - Solusi: Merapikan struktur file dan memastikan hanya satu NewsController yang aktif untuk endpoint API.

2. Sinkronisasi Properti DTO (Error CS1061):
   - Masalah: Properti Name dan CreateDate tidak terbaca pada model NewsItemDto.
   - Solusi: Melakukan pemetaan ulang (mapping) menggunakan properti yang benar, yaitu Title dan PublishDate.

3. Integrasi Navigasi:
   - Masalah: Menghubungkan judul berita di React agar bisa mengarah ke halaman detail di Umbraco.
   - Solusi: Menambahkan properti URL secara dinamis pada JSON response agar navigasi ke Razor Detail View berjalan lancar.

4. Encoding File:
   - Masalah: Muncul peringatan pengkodean teks saat menyimpan file.
   - Solusi: Menggunakan format teks standar tanpa karakter khusus untuk memastikan kompatibilitas sistem.

---

Terima kasih atas kesempatannya. Saya sangat menikmati proses pengerjaan tugas integrasi ini!

Salam, 
Ilham Nur Fadillah
