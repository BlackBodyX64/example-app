FROM webdevops/php-apache:8.0-alpine

COPY ./dockerizer/php.ini /opt/docker/etc/php/php.ini
COPY ./dockerizer/vhost.conf /opt/docker/etc/httpd/vhost.conf
COPY composer.json composer.lock /app/
RUN composer install --no-interaction --no-scripts --no-suggest
COPY . /app