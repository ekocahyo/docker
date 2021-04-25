# Docker for local development
## How to use!
Before clone, you must install docker engine and docker-compose. Open your terminal and type this command:
```sh
git clone git@github.com:ekocahyo/docker.git
cd docker
mkdir server/postgres/data
docker-compose up -d
```

You can run only a few services. Ex:
```sh
docker-compose stop
docker start nginx php-fpm redis
```

## Features

- Web server (nginx)
- php include composer versi 7 (latest => 7.4)
- MySQL (MariaDB latest)
- PostgreSQL (latest)
- MongoDB (latest)
- RabbitMQ (management latest)
- Mailhog (latest)

## How to install yii
```sh
docker exec -it php-fpm sh
composer create-project --prefer-dist yiisoft/yii2-app-basic yii
exit
```

## How to install laravel
```sh
docker exec -it php-fpm sh
composer create-project laravel/laravel laravel
exit
```

## How to use composer
```sh
docker exec -it php-fpm sh
cd  to-path-your-project
composer install
exit
```

## How update config a service
If you need update config a service like parameter on php-fpm. change the ``server/php/fpm.d/www.conf`` file and then rebuild service:
```sh
docker-compose stop php-fpm
docker-compose up -d --build php-fpm
```