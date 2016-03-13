FROM ubuntu:15.10
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apt-get update -y ; \
    apt-get install -y vim wget git zsh ; \
    cd /root ; \
    wget --no-check-certificate -O - https://raw.github.com/twolights/meowrc/master/setup.sh | bash

ENTRYPOINT ["zsh"]
