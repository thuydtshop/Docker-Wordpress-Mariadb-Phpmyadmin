# Try to change the php version for compatibility with your Opencart version
FROM php:8.1.8-apache

RUN a2enmod rewrite headers

RUN apt-get update && \
    apt-get install -y --no-install-recommends git zip libzip-dev

RUN set -xe \
    && apt update \
    && apt install -y libpng-dev libjpeg-dev libwebp-dev unzip \
    && rm -rf /var/lib/apt/lists/* \
    && docker-php-ext-configure gd --with-jpeg=/usr --with-webp=/usr \
    && docker-php-ext-install gd mysqli pdo_mysql zip \
    && chown -R www-data:www-data /var/www/html
