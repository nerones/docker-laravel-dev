FROM nerones/simple-php-apache-dev:5.6.17
RUN curl -sL https://deb.nodesource.com/setup_4.x | bash - \
    && apt-get -y install openssh-client git nodejs curl --no-install-recommends \
    && rm -rf /var/lib/apt/lists/* \
    && curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer \
    && npm install -g gulp
