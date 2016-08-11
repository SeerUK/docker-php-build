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
        php5.6 \
        php5.6-cli \
        php5.6-common \
        php5.6-curl \
        php5.6-dev \
        php5.6-fpm \
        php5.6-gd \
        php5.6-imagick \
        php5.6-intl \
        php5.6-json \
        php5.6-mcrypt \
        php5.6-memcached \
        php5.6-mysql \
        php5.6-zip \
    && apt-get autoremove \
    && apt-get clean \
    && rm -rf /var/lib/app/lists/*

CMD php -v
