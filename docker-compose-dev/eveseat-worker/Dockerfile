FROM php:7.2-alpine

RUN apk add --no-cache git zip unzip curl \
    libpng-dev bzip2-dev icu-dev && \
    docker-php-ext-install pdo_mysql gd bz2 intl pcntl

VOLUME /var/www
WORKDIR /var/www/seat

COPY startup.sh /root/startup.sh
RUN chmod +x /root/startup.sh

ENTRYPOINT ["/bin/sh", "/root/startup.sh"]
