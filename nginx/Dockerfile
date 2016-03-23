FROM twolights/base-alpine:latest
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apk add --update nginx ; \
    rm -fr /var/cache/apk/*

EXPOSE 80
ENTRYPOINT ["nginx"]
CMD ["-g", "daemon off;"]
