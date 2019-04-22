FROM php:7.1-apache

RUN docker-php-ext-install mysqli
RUN docker-php-ext-install mbstring
RUN docker-php-ext-install pdo_mysql

RUN pecl install xdebug-2.6.0
RUN docker-php-ext-enable xdebug

RUN apt-get update&& apt-get install -y \
   libxml2-dev \
   libzip-dev \
   zlib1g-dev \
       && docker-php-ext-install zip

RUN a2enmod rewrite

WORKDIR /var/www/html

CMD bash -c "nohup php composer.phar install && apache2-foreground"
