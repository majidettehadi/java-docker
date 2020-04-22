FROM majid7221/debian:stretch

ENV LANG C.UTF-8

ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64
ENV PATH $JAVA_HOME/bin:$PATH

RUN set -ex \
    && mkdir /usr/share/man/man1 \
    && apt-get update \
    && apt-get install -y --no-install-recommends \
        openjdk-8-jdk-headless \
        libtcnative-1 \
        maven \
    && rm -rf usr/share/man/man1 \
    && rm -rf /var/lib/{apt,dpkg,cache,log}/ /tmp/* /var/tmp/*
