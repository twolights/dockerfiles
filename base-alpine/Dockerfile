FROM alpine:3.3
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apk add --update vim wget git zsh bash ; \
    cd /root ; \
    wget --no-check-certificate -O - https://raw.github.com/twolights/meowrc/master/setup.sh | bash ; \
    rm -fr /var/cache/apk/*

ENTRYPOINT ["zsh"]
