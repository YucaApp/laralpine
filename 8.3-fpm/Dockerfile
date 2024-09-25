FROM php:8.3-fpm-alpine
# Install the php extension installer from its image
COPY --from=mlocati/php-extension-installer /usr/bin/install-php-extensions /usr/local/bin/
# Install dependencies
RUN apk add --no-cache \
    openssl \
    ca-certificates \
    libxml2-dev \
    oniguruma-dev
# Install php extensions
RUN install-php-extensions \
    bcmath \
    pdo_mysql \
    pcntl \
    redis-stable