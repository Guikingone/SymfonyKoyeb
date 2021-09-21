FROM webdevops/php-nginx:8.0-alpine

ENV WEB_DOCUMENT_ROOT /srv/app/public

COPY --from=composer:latest /usr/bin/composer /usr/bin/composer

WORKDIR /srv/app
COPY . .

RUN composer install --no-interaction --optimize-autoloader
