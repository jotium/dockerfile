FROM php:latest

RUN curl -LsS http://symfony.com/installer -o /usr/local/bin/symfony \
 && chmod a+x /usr/local/bin/symfony \
 && echo "date.timezone=${PHP_TIMEZONE:-UTC}" > /usr/local/etc/php/conf.d/date_timezone.ini

WORKDIR "/usr/src/app"

CMD ["-"] 
ENTRYPOINT ["symfony"] 
