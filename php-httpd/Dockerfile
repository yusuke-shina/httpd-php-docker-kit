ARG PHP_IMAGE_VERSION=apache
FROM php:${PHP_IMAGE_VERSION}

RUN apt-get upgrade && \
    apt-get update && \
    apt-get install -y \
      vim \
      libonig-dev && \
    docker-php-ext-install \
      pdo_mysql \
      mysqli \
      mbstring && \
    a2enmod rewrite && \
    echo "ServerName localhost" | tee /etc/apache2/conf-available/fqdn.conf

WORKDIR /var/www/html
