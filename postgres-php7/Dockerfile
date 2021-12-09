FROM php:7-apache

RUN set -x && \
  apt-get -y update && \
  apt-get install -y --no-install-recommends  libicu-dev libpq-dev  && \
  NPROC=$(grep -c ^processor /proc/cpuinfo 2>/dev/null || 1) && \
  docker-php-ext-install -j${NPROC} intl && \
  docker-php-ext-install -j${NPROC} pdo_pgsql && \
  docker-php-ext-install -j${NPROC} pdo_mysql && \
  rm -rf /tmp/pear