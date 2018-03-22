FROM phpdockerio/php71-fpm:latest

# Install selected extensions and other stuff
RUN apt-get update \
    && apt-get -y --no-install-recommends install openssh-client git php7.1-mysql php7.1-gd php7.1-mbstring php7.1-intl \
    && apt-get clean; rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* /usr/share/doc/*
RUN usermod -u 1000 www-data

ENV PATH="/application/vendor/bin:${PATH}"

WORKDIR "/application"