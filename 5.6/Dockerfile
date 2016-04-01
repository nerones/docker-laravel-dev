FROM nerones/simple-php-apache-dev:5.6.17
RUN curl -sL https://deb.nodesource.com/setup_4.x | bash -
RUN apt-get -y install openssh-client git nodejs curl chrpath libssl-dev libxft-dev libfreetype6 libfreetype6-dev libfontconfig1 libfontconfig1-dev --no-install-recommends \
    && rm -rf /var/lib/apt/lists/* \
    && curl -sS https://getcomposer.org/installer | php \
    && mv composer.phar /usr/local/bin/composer \
    && npm install -g bower gulp laravel-elixir@^3.0.0
RUN rm /usr/local/etc/php/conf.d/xdebug.ini
RUN mkdir /selenium \
    && cd /selenium \
    && curl -sL http://goo.gl/IHP6Qw -o selenium-standalone-server.jar \
    && chmod +x selenium-standalone-server.jar \
    && curl -sL https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2 -o phantomjs-2.1.1-linux-x86_64.tar.bz2 \
    && tar xf phantomjs-2.1.1-linux-x86_64.tar.bz2 \
    && chmod +x phantomjs-2.1.1-linux-x86_64 \
    && mv phantomjs-2.1.1-linux-x86_64 /usr/local/bin/
