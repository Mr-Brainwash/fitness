FROM php:8.3-fpm

COPY --from=composer /usr/bin/composer /usr/bin/composer
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/bin/

RUN install-php-extensions zip
RUN apt-get update && apt-get install -y --no-install-recommends unzip

CMD ["php-fpm"]