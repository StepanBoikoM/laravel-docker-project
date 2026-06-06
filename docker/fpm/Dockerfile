FROM php:8.2-fpm-alpine

RUN apk add --no-cache postgresql-dev \
    && docker-php-ext-install pdo_pgsql

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /var/www/html

RUN chown -R www-data:www-data /var/www/html
