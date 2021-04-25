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

## How to use composer
```sh
docker exec -it php-fpm sh
cd  to-path-your-project
composer install
exit
```