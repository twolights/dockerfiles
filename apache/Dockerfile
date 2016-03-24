FROM twolights/base-alpine:latest
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apk add --update apache2 apache2-ssl apache2-proxy apache2-utils ; \
    mkdir /var/run/apache2 ; \
    chown apache:apache /var/run/apache2 ; \
    rm -fr /etc/apache2/ ; \
    rm -fr /var/cache/apk/*

COPY etc /etc/apache2

EXPOSE 80
EXPOSE 443
ENTRYPOINT ["httpd"]
CMD ["-f", "/etc/apache2/httpd.conf", "-d", "/etc/apache2", "-DFOREGROUND"]
