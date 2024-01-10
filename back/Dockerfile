FROM php:8.3.1-fpm

WORKDIR /var/www/back

COPY . /var/www/back

RUN apt-get update && \
    apt-get install -y \
    nginx \
    nodejs \
    npm \
    default-mysql-client \
    && rm -rf /var/lib/apt/lists/* \
    && docker-php-ext-install pdo_mysql \
    && pecl install redis \
    && docker-php-ext-enable redis \
    && curl -sS https://getcomposer.org/installer | php -- --install-dir=/usr/local/bin

CMD ["php-fpm"]

EXPOSE 9000
