# Filament RichEditor + Spatie Translatable (Issue Reproduction)

This repository demonstrates a bug where, when using **Filament 4 `RichEditor`** with **Spatie Translatable**, the active locale saves as **HTML**, while other locales save as **ProseMirror JSON**.

## Stack
- **PHP**: 8.3+
- **Laravel**: 12.x
- **Filament**: 4.x
- **spatie/laravel-translatable**: 6.x
- **DB**: SQLite (default)
- **Node**: 18+ (for Vite)

## Quick Start

```bash
# 1) Clone the repo
git clone https://github.com/broqit/filament-richeditor-issue.git
cd filament-richeditor-issue

# 2) Install PHP dependencies
composer install

# 3) Copy env file
cp .env.example .env

# 4) Generate app key and run migrations
php artisan key:generate
php artisan migrate --seed  # if seeders exist, otherwise just `php artisan migrate`

# 5) Create an admin user for Filament
php artisan make:filament-user
# Enter name, email, password → use them to log in at /admin

# 6) Install frontend dependencies
npm install
npm run dev   # or npm run build

# 7) Start the server
php artisan serve
