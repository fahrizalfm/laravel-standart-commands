# BASIC RESET CONFIGURATION LARAVEL
### Reset semuanya agar project jalan seperti semula (baru clone atau buat baru)
- composer install
- php artisan key:generate
- php artisan migrate --seed
- php artisan storage:link
- php artisan config:clear
- php artisan cache:clear
- php artisan route:clear
- php artisan view:clear
### Mengubah konfigurasi di .env atau config/*.php
- php artisan config:clear
- php artisan config:cache   # (opsional, untuk cache ulang)
### Laravel seperti tidak membaca perubahan (bersihkan semua cache saat debugging error)
- php artisan optimize:clear
- composer dump-autoload
### Reset database
- php artisan migrate:fresh --seed
### Ubah file routes/web.php atau api.php
- php artisan route:clear
- php artisan route:cache    # (jika semua route bukan closure)
### Kelola seeder
- php artisan db:seed --class=UsersTableSeeder (jalankan seeder tertentu)
- php artisan db:seed (jalankan semua seeder)
