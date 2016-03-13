FROM twolights/base:latest
MAINTAINER Evan Chen <twolights@gmail.com>

RUN apt-get install -y clang libicu-dev libssl-dev libxml2-dev libpython2.7-dev ; \
    wget -q -O - https://swift.org/keys/all-keys.asc | gpg --import - ; \
    cd /root ; \
    wget 'https://swift.org/builds/development/ubuntu1510/swift-DEVELOPMENT-SNAPSHOT-2016-02-25-a/swift-DEVELOPMENT-SNAPSHOT-2016-02-25-a-ubuntu15.10.tar.gz' ; \
    wget 'https://swift.org/builds/development/ubuntu1510/swift-DEVELOPMENT-SNAPSHOT-2016-02-25-a/swift-DEVELOPMENT-SNAPSHOT-2016-02-25-a-ubuntu15.10.tar.gz.sig' ; \
    if gpg --keyserver hkp://pool.sks-keyservers.net --refresh-keys Swift ; then \
        tar zxfv swift-DEVELOPMENT-SNAPSHOT-2016-02-25-a-ubuntu15.10.tar.gz ; \
        cp -R swift-DEVELOPMENT-SNAPSHOT-2016-02-25-a-ubuntu15.10/usr/* /usr ; \
        rm -fr swift-DEV* ; \
    else echo "Swift source signature validation failed!" ; \
    fi

ENTRYPOINT ["swift"]
