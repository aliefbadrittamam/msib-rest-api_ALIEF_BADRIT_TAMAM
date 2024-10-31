# MSIB REST API
Proyek ini adalah sebuah REST API yang dikembangkan untuk memenuhi tugas MSIB. API ini menggunakan Laravel dengan middleware Sanctum untuk proteksi endpoint dan memiliki berbagai fitur seperti registrasi, login, manajemen produk, dan pencarian produk.

### Dibuat oleh: FSD 25 - ALIEF BADRIT TAMAM

## Daftar Tugas Pengembangan
1. **Tambahkan Function Logout**
   - Menyediakan endpoint logout bagi pengguna yang telah login.

2. **Modifikasi Route `api.php`**
   - Melindungi endpoint dengan middleware Sanctum
   - Memastikan hanya pengguna terautentikasi yang dapat mengakses

3. **Buat Endpoint Pencarian Produk**
   - Mengimplementasikan pencarian produk berdasarkan nama

4. **Modifikasi Endpoint Produk**
   - Menambahkan fitur filter berdasarkan kategori

## Fitur Utama API

### Autentikasi
- Registrasi pengguna baru
- Login pengguna
- Logout pengguna
- Proteksi endpoint menggunakan Sanctum

### Manajemen Produk
- List produk keseluruhan
- Pencarian produk berdasarkan nama
- Filter produk berdasarkan kategori
- Update informasi produk

## Persyaratan Sistem
- PHP 8.x
- Composer
- Laravel Framework
- Database MySQL/MariaDB

## Langkah Instalasi

### Prasyarat
- Pastikan PHP, Composer, dan MySQL terinstal
- Clone repositori dari GitHub

### Instalasi Proyek
1. Clone repositori
   ```bash
   git clone https://github.com/siitinurhaliza/msib-rest-api_SITI-NURHALIZA.git
   ```

2. Masuk ke direktori proyek
   ```bash
   cd msib-rest-api_SITI-NURHALIZA
   ```

3. Install dependencies
   ```bash
   composer install
   ```

4. Salin file environment
   ```bash
   cp .env.example .env
   ```

5. Generate application key
   ```bash
   php artisan key:generate
   ```

6. Konfigurasi database di file `.env`

7. Jalankan migrasi database
   ```bash
   php artisan migrate
   ```

8. Jalankan server
   ```bash
   php artisan serve
   ```

## Endpoint API

### Autentikasi
- `POST /api/register` - Registrasi pengguna baru
- `POST /api/login` - Login pengguna
- `POST /api/logout` - Logout pengguna (memerlukan autentikasi)

### Produk
- `GET /api/products` - Daftar produk (dengan opsional filter kategori)
- `GET /api/products/search` - Pencarian produk berdasarkan nama
- `POST /api/products` - Tambah produk baru
- `PUT /api/products/{id}` - Update produk

## Autentikasi & Keamanan
- Menggunakan Laravel Sanctum
- Token-based authentication
- Proteksi endpoint dengan middleware

## Kontributor
- ALIEF BADRIT TAMAM (FSD 25)

## Lisensi
[Tentukan lisensi proyek Anda]
