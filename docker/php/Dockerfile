FROM php:8.4-fpm

RUN apt-get update && apt-get upgrade

RUN apt-get install -y libpng-dev \
        libjpeg-dev \
        libfreetype6-dev \
        libzip-dev \
        unzip \
        git \
        libonig-dev \
        libxml2-dev \
        curl \
        bash \
        gcc make autoconf libc-dev pkg-config \
        && docker-php-ext-configure gd \
        && docker-php-ext-install gd soap zip pcntl bcmath

EXPOSE 9000

CMD ["php-fpm"]



