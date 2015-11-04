FROM nerones/simple-php-apache-dev:5.6.14
RUN apt-get update \
    && apt-get -y install nodejs-legacy npm curl --no-install-recommends \
    && rm -rf /var/lib/apt/lists/* \
    && curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer \
    && npm install -g gulp laravel-elixir
