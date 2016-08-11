FROM ubuntu:xenial
MAINTAINER Elliot Wright <hello@elliotdwright.com>

# Install PHP
RUN set -x \
    && useradd -u 1000 -m -s /bin/bash php \
    && mkdir -p /app \
    && chown -R php: /app \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        language-pack-en-base \
        software-properties-common \
    && LC_ALL=en_US.UTF-8 apt-add-repository ppa:ondrej/php \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        php7.1 \
        php7.1-cli \
        php7.1-common \
        php7.1-curl \
        php7.1-dev \
        php7.1-fpm \
        php7.1-gd \
        php7.1-imagick \
        php7.1-intl \
        php7.1-json \
        php7.1-mcrypt \
        php7.1-memcached \
        php7.1-mysql \
        php7.1-zip \
    && apt-get autoremove \
    && apt-get clean \
    && rm -rf /var/lib/app/lists/*

CMD php -v
