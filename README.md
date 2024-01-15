# laravel-environment

#### Create new Laravel project
```
docker exec -it fpm-laravel-environment composer create-project laravel/laravel /var/www/
```

#### Recreate APP_KEY .env
```
docker exec -it fpm-laravel-environment php /var/www/artisan key:generate --ansi
```
#### Create table migration
```
docker exec -it fpm-laravel-environment php /var/www/artisan migrate:install
```
#### Reset database
```
docker exec -it fpm-laravel-environment php /var/www/artisan migrate:fresh
```
#### Create Seed data
```
docker exec -it fpm-laravel-environment php /var/www/artisan migrate --seed
```
