FROM php:apache

MAINTAINER Vladislav Vlastovskiy <me@vlastv.ru>

RUN apt-get update && apt-get install -y \
        libfreetype6-dev \
        libjpeg62-turbo-dev \
        libpng12-dev \
    && docker-php-ext-install mbstring mysql \
    && docker-php-ext-configure gd --with-freetype-dir=/usr/include/ --with-jpeg-dir=/usr/include/ \
    && docker-php-ext-install gd \
    && echo 'memory_limit=128M\nallow_url_fopen=On\nsafe_mode=Off\nmbstring.func_overload=0\nshort_open_tag=On\nzend.ze1_compatibility_mode=Off\nmbstring.internal_encoding=UTF-8\n' > $PHP_INI_DIR/conf.d/netcat.ini
    
VOLUME /var/www/html/netcat_files \
       /var/www/html/netcat_cache \
       /var/www/html/netcat_trash \
       /var/www/html/netcat_dump \
       /var/www/html/netcat/tmp
