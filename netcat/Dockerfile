FROM php:apache
MAINTAINER Vladislav Vlastovskiy <me@vlastv.ru>

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libmcrypt-dev \
        libpng12-dev \
    && docker-php-ext-install mysql gd mbstring

VOLUME /var/www/html/netcat_files \
       /var/www/html/netcat_cache \
       /var/www/html/netcat_trash \
       /var/www/html/netcat_dump \
       /var/www/html/netcat/tmp
