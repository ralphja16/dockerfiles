# Pull base image
FROM phalconphp/build:debian-stretch

LABEL maintainer="Serghei Iakovlev <serghei@phalconphp.com>"

RUN apt-get clean -y \
    && wget -O /etc/apt/trusted.gpg.d/php.gpg https://packages.sury.org/php/apt.gpg \
    && echo "deb https://packages.sury.org/php/ $(lsb_release -sc) main" > /etc/apt/sources.list.d/php.list \
    && /usr/local/bin/apt-upgrade \
    && /usr/local/bin/apt-install \
        php7.1-dev \
        php7.1-common \
        php7.1-cli \
    && apt-get autoremove -y \
    && apt-get autoclean -y \
    && apt-get clean -y \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
