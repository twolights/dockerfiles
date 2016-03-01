FROM twolights/swift
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apt-get update -y ; \
    apt-get install -y lsb-release git uuid-dev libcurl4-openssl-dev libevent-pthreads-2.0-5 libevent-dev libsqlite3-dev ; \
    hash ; \
    cd /root ; \
    git clone https://github.com/PerfectlySoft/Perfect ; \
    cd Perfect/PerfectLib/ ; \
    make all install ; \
    cd ../PerfectServer/ ; \
    make all install ; \
    cd ../ ; \
    rm -fr Perfect/

ENTRYPOINT ["bash"]
