# SepatuStore - Toko Sepatu Online

[![Laravel](https://img.shields.io/badge/Laravel-11.x-FF2D20?style=for-the-badge&logo=laravel)](https://laravel.com)
[![PHP](https://img.shields.io/badge/PHP-8.2+-777BB4?style=for-the-badge&logo=php)](https://php.net)
[![Filament](https://img.shields.io/badge/Filament-3.x-1f2937?style=for-the-badge&logo=filament)](https://filamentphp.com)

SepatuStore adalah aplikasi web e-commerce modern untuk penjualan sepatu online yang dibangun menggunakan Laravel 11 dan FilamentPHP. Aplikasi ini menyediakan platform lengkap untuk mengelola toko sepatu dengan fitur admin panel yang powerful dan user-friendly.

## 🚀 Fitur Utama

### ✨ Fitur Admin (FilamentPHP)
- **Dashboard Analytics** - Ringkasan penjualan dan statistik toko
- **Manajemen Produk** - CRUD lengkap untuk sepatu dengan multiple foto
- **Manajemen Kategori** - Pengelolaan kategori sepatu
- **Manajemen Brand** - Pengelolaan merek sepatu
- **Manajemen Ukuran** - Pengelolaan variasi ukuran sepatu
- **Manajemen Transaksi** - Tracking dan pengelolaan pesanan
- **Kode Promo** - Sistem diskon dan voucher
- **Manajemen Pengguna** - Pengelolaan data customer

## 📋 Struktur Database

### Model Utama:
- `User` - Data pengguna dan customer
- `Shoe` - Produk sepatu utama
- `Brand` - Merek sepatu
- `Category` - Kategori sepatu
- `ShoeSize` - Variasi ukuran sepatu
- `ShoePhoto` - Galeri foto produk
- `ProductTransaction` - Data transaksi pembelian
- `PromoCode` - Kode diskon dan voucher

## 🛠️ Tech Stack

- **Backend**: Laravel 11.x (PHP 8.2+)
- **Frontend**: Livewire, Tailwind CSS
- **Admin Panel**: FilamentPHP 3.x
- **Build Tool**: Vite
- **Database**: SQLite (default)
- **Development**: Laravel Sail (Docker)

## 📦 Instalasi

### Prerequisites
- PHP 8.2 atau lebih tinggi
- Composer
- Node.js & npm
- Git

### Langkah Instalasi

1. **Clone Repository**
   ```bash
   git clone <repository-url>
   cd sepatustorebwa
   ```

2. **Install PHP Dependencies**
   ```bash
   composer install
   ```

3. **Install Node Dependencies**
   ```bash
   npm install
   ```

4. **Setup Environment**
   ```bash
   cp .env.example .env
   php artisan key:generate
   ```

5. **Database Setup**
   ```bash
   # Untuk SQLite (default)
   touch database/database.sqlite

   # Untuk MySQL (opsional)
   # Update konfigurasi DB di file .env
   # DB_CONNECTION=mysql
   # DB_HOST=127.0.0.1
   # DB_PORT=3306
   # DB_DATABASE=sepatustore
   # DB_USERNAME=your_username
   # DB_PASSWORD=your_password
   ```

6. **Run Migrations**
   ```bash
   php artisan migrate
   ```

7. **Build Assets**
   ```bash
   npm run build
   # atau untuk development
   npm run dev
   ```

## 📖 Penggunaan

### Akses Admin Panel
1. Buka browser dan akses: `http://localhost:8000/admin`
2. Login dengan kredensial default atau buat user admin baru
3. Kelola produk, kategori, brand, dan transaksi melalui dashboard

### Development Commands
```bash
# Menjalankan semua services (server, queue, logs, vite)
composer run dev

# Menjalankan tests
php artisan test

# Code formatting
./vendor/bin/pint

# Generate API documentation (jika ada)
php artisan scribe:generate
```

## 🔧 Konfigurasi

### Environment Variables (.env)
```env
APP_NAME="SepatuStore"
APP_ENV=local
APP_KEY=base64:your-key-here
APP_DEBUG=true
APP_URL=http://localhost:8000

DB_CONNECTION=sqlite
# DB_CONNECTION=mysql (untuk MySQL)

MAIL_MAILER=log
# MAIL_MAILER=smtp (untuk email)

VITE_APP_NAME="${APP_NAME}"
```

### File Konfigurasi Penting
- `config/filament.php` - Konfigurasi admin panel
- `tailwind.config.js` - Konfigurasi styling
- `vite.config.js` - Konfigurasi build tool

## 📁 Struktur Project

```
sepatustorebwa/
├── app/
│   ├── Filament/Resources/     # Admin panel resources
│   ├── Http/Controllers/       # HTTP controllers
│   ├── Livewire/              # Livewire components
│   ├── Models/                # Eloquent models
│   ├── Repositories/          # Repository pattern
│   └── Services/              # Business logic services
├── database/
│   ├── migrations/            # Database migrations
│   └── seeders/               # Database seeders
├── public/                    # Public assets
├── resources/
│   ├── css/                   # Custom CSS
│   ├── js/                    # JavaScript files
│   └── views/                 # Blade templates
├── routes/                    # Route definitions
├── storage/                   # File storage
└── tests/                     # Test files
```
---

**SepatuStore** - Aplikasi toko sepatu modern untuk bisnis Anda! 👟✨
