FROM php:8.0-fpm

RUN apt-get update > /dev/null && apt-get install -y

# Install Composer
RUN curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin --filename=composer > /dev/null

RUN usermod -u 1000 www-data

RUN chown -R www-data:1000 /var/www

USER www-data

WORKDIR /var/www