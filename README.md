# Sweet Crust Bakery - Inventory System

Aplikasi sistem manajemen stok dan inventaris untuk toko toyi **Sweet Crust Bakery**. Proyek mini ini dibangun menggunakan framework **Laravel** 
dengan menerapkan pola arsitektur **MVC (Model-View-Controller**.

## Fitur Utama
- Manajemen Produk Bakery: Mencatat data roti/ kue beserta SKU, harga, dan stok.
- Indikator Stok Menipis: Peringatan otomatis jika stok produk berada di bawah batas minimum.
- Pencatatan Riwayat Stok: Pelacakan masuk dan keluarnya stok barang ('Stock Movement').
- Kategori Produk: Pengelompokan produk berdasarkan jenisnya.

## Struktur Arsitektur MVC

Aplikasi ini disusun berdasarkan struktur komponen standar Laravel:

- Models (`app/Models/`)
  - `Category.php` - Model untuk data kategori produk.
  - `Product.php` - Model utama untuk produk bakery dan logika relasi stok.
  - `StockMovement.php` - Model riwayat transaksi masuk/keluar stok.

- Controllers (`app/Http/Controllers/`)
  - `ProductController.php` - Mengelola logika menampilkan daftar produk dan penambahan stok baru.

- Migrations (`database/migrations/`)
  - `create_bakery_tables.php` - Skema basis data untuk tabel `categories`, `products`, dan `stock_movements`.

- Views (`resources/views/`)
  - `layouts/app.blade.php` - Template tampilan utama (menggunakan Bootstrap 5).
  - `products/index.blade.php` - Tampilan antarmuka daftar stok dan modal tambah produk.

- Routes (`routes/`)
  - `web.php` - Pemetaan URL/endpoint untuk aplikasi.
 
## Cara Menjalankan Project (Local Development).

1. Clone Repository
   ```bash
   git clone [https://github.com/USERNAME_KAMU/bakery-sweetcrust.git](https://github.com/USERNAME_KAMU/bakery-sweetcrust.git)
   cd bakery-sweetcrust

2. Install Dependensi PHP
   bash
   composer install

3. Konfigurasi Enviroment
   Salin file .env.example menjadi .env, lalu atur koneksi database:
   cp .env.example .env
   php artisan key:generate

4. Jalankan Migration
   bash
   php artisan migrate

5. Jalankan Server
   bash
   php artisan serve
   
   Akses aplikasi di browser melalui http://127.0.0.1:8000.
