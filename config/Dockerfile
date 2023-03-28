FROM wordpress:php8.2-fpm-alpine

RUN apk --update add zip unzip gcc make g++ zlib-dev autoconf yarn automake libpng-dev alpine-sdk nasm net-tools linux-headers
RUN pecl install xdebug
RUN docker-php-ext-enable xdebug
#ADD https://github.com/composer/getcomposer.org/raw/master/web/installer composer-setup.php
ADD https://getcomposer.org/download/latest-stable/composer.phar /usr/local/bin/composer
#RUN php composer-setup.php --install-dir=/usr/bin --filename=composer && rm composer-setup.php
COPY ./entrypoint.sh /usr/bin/entrypoint.sh
RUN chmod 777 /usr/bin/entrypoint.sh
