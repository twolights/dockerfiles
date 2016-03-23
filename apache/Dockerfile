FROM twolights/base-alpine:latest
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apk add --update apache2 apache2-proxy apache2-utils ; \
    rm -fr /etc/apache2/ ; \
    rm -fr /var/cache/apk/*
COPY etc /etc/apache2

EXPOSE 80
EXPOSE 443
ENTRYPOINT ["httpd"]
CMD ["-f", "/etc/apache2/apache2.conf", "-d", "/etc/apache2", "-DFOREGROUND"]
