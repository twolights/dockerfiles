FROM twolights/base-alpine:latest
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apk add --update php-fpm php-dev php-phar php-mcrypt php-mysql php-gd php-pear php-json ; \
    rm -fr /etc/php* ; \
    rm -fr /var/cache/apk/*
COPY etc /etc/php5

EXPOSE 9000
ENTRYPOINT ["php-fpm"]
CMD ["-F", "-y", "/etc/php5/fpm/php-fpm.conf"]
