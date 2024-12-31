# Portal Berita Winnicode

Portal Berita Winnicode adalah aplikasi web berbasis Laravel yang dirancang untuk menyediakan platform berita dengan fitur modern. Proyek ini memungkinkan pengguna untuk membaca, mengelola, dan mengunggah berita dengan antarmuka yang ramah pengguna.

## Prasyarat
Sebelum memulai, pastikan Anda memiliki:

1. **PHP** >= 8.0
2. **Composer**
3. **Node.js** dan **npm**
4. **Database** (MySQL atau MariaDB)
5. **Git** (opsional, jika ingin mengelola repositori)

## Langkah Instalasi

Ikuti langkah-langkah berikut untuk mengatur proyek:

1. **Kloning Proyek**
   ```bash
   git clone <repository-url>
   cd PortalBerita_Winnicode
   ```

2. **Instal Dependensi PHP**
   ```bash
   composer install
   ```

3. **Instal Dependensi Node.js**
   ```bash
   npm install
   ```

4. **Salin File .env**
   Salin file `.env.example` menjadi `.env`:
   ```bash
   cp .env.example .env
   ```

5. **Atur Konfigurasi Database**
   Buka file `.env` dan sesuaikan pengaturan berikut:
   ```env
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=nama_database
   DB_USERNAME=username_database
   DB_PASSWORD=password_database
   ```

6. **Generate Application Key**
   Jalankan perintah berikut untuk menghasilkan kunci aplikasi:
   ```bash
   php artisan key:generate
   ```

7. **Migrasi dan Seed Database**
   Buat tabel dan data awal dengan menjalankan perintah:
   ```bash
   php artisan migrate --seed
   ```

## Cara Menjalankan

1. **Jalankan Server Lokal**
   Untuk menjalankan server lokal, gunakan perintah berikut:
   ```bash
   php artisan serve
   ```
   Akses aplikasi di [http://localhost:8000](http://localhost:8000).

2. **Kompilasi Asset Frontend**
   Jalankan perintah berikut untuk memantau perubahan pada file frontend:
   ```bash
   npm run dev
   ```

## Ekspor Database
Jika diperlukan, Anda dapat mengekspor database menggunakan perintah berikut di MySQL:

```sql
mysqldump -u username_database -p nama_database > nama_file.sql
```

## Catatan
- Pastikan semua dependensi dan konfigurasi telah diatur dengan benar sebelum menjalankan aplikasi.
- Jika mengalami masalah, periksa log Laravel di `storage/logs/laravel.log`.

