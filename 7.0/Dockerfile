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
        git-core \
        php7.0 \
        php7.0-cli \
        php7.0-common \
        php7.0-curl \
        php7.0-dev \
        php7.0-fpm \
        php7.0-gd \
        php7.0-imagick \
        php7.0-intl \
        php7.0-json \
        php7.0-mcrypt \
        php7.0-memcached \
        php7.0-mysql \
        php7.0-zip \
    && apt-get autoremove \
    && apt-get clean \
    && rm -rf /var/lib/app/lists/*

CMD php -v
