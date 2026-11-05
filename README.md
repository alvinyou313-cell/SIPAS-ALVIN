# SIPAS - Sistem Informasi Pengaduan Sarana Sekolah

Project akhir semester gasal XII RPL, Presensi 3.

## Fitur
- Login/logout multi-role Admin & Siswa
- Dashboard Admin dan Siswa
- CRUD kategori sarana
- Manajemen pengguna
- Pengajuan pengaduan + upload foto
- Status Pending, Approved, Rejected, Selesai
- Tanggapan Admin
- Riwayat pengaduan siswa
- Laporan dan cetak
- Migration + Seeder
- UI responsive Bootstrap 5

## Kebutuhan
- PHP 8.2+
- Composer
- MySQL/MariaDB
- Laravel 12

## Instalasi Windows / VS Code
1. Extract ZIP.
2. Buka folder `SIPAS` di VS Code.
3. Buka Terminal.
4. Jalankan:
   ```
   composer install
   copy .env.example .env
   php artisan key:generate
   ```
5. Buat database MySQL bernama `sipas` melalui phpMyAdmin atau MySQL.
6. Pastikan `.env` berisi:
   ```
   DB_CONNECTION=mysql
   DB_HOST=127.0.0.1
   DB_PORT=3306
   DB_DATABASE=sipas
   DB_USERNAME=root
   DB_PASSWORD=
   ```
7. Jalankan:
   ```
   php artisan migrate --seed
   php artisan storage:link
   php artisan serve
   ```
8. Buka `http://127.0.0.1:8000`.

## Akun Demo
### Admin
Email: `admin@sipas.test`
Password: `admin123`

### Siswa
Email: `siswa@sipas.test`
Password: `siswa123`

## Alur utama
Siswa login -> membuat pengaduan -> sistem menyimpan status Pending -> Admin memverifikasi -> Approved/Rejected -> jika diproses, Admin mengubah menjadi Selesai -> siswa melihat status/riwayat.
