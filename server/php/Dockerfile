FROM php:7-fpm-alpine

RUN docker-php-ext-install mysqli && \
    docker-php-ext-install json && \
    docker-php-ext-install pdo_mysql &&\
    docker-php-source delete && \
    rm -fv /usr/local/etc/php-fpm.d/* && \
    apk add --no-cache composer && \
    rm -rf /tmp/* /usr/local/lib/php/doc/* /var/cache/apk/*

WORKDIR /www

CMD ["php-fpm"]