# Laravel-postgres-nginx-docker-sample

 * docker
 * nginx
 * postgres
 * laravel

でマイグレーションまで試すサンプル.

## 実行

```
docker-compose build
docker-compose up -d
docker-compose exec php-fpm sh
cd /var/www/html/testapp
php artisan migrate
```
