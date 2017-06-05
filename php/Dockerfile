FROM php:7-apache
RUN a2enmod rewrite
RUN a2enmod socache_memcache.load
RUN service apache2 restart

COPY php.ini /usr/local/etc/php/


RUN apt-get update \
  && apt-get install -y libfreetype6-dev libjpeg62-turbo-dev libpng12-dev libmcrypt-dev \
  && docker-php-ext-install pdo_mysql mysqli mbstring gd iconv mcrypt


RUN apt-get install git --assume-yes
RUN apt-get install zip unzip --assume-yes
RUN apt-get install libmemcached-dev --assume-yes



RUN apt-get install memcached --assume-yes




RUN curl -sS https://getcomposer.org/installer | \
    php -- --install-dir=/usr/bin/ --filename=composer

