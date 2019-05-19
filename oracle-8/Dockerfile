FROM majid7221/debian:stretch

RUN set -ex \
    && apt-key adv --no-tty --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EEA14886 \
    && echo "deb http://ppa.launchpad.net/webupd8team/java/ubuntu xenial main" > /etc/apt/sources.list.d/webupd8team-java.list \
    && echo oracle-java8-installer shared/accepted-oracle-license-v1-1 select true | debconf-set-selections \
    && mkdir /usr/share/man/man1 \
    && apt-get update \
    && apt-get install -y oracle-java8-installer \
    && rm -rf /var/lib/{apt,dpkg,cache,log}/ /tmp/* /var/tmp/*

ENV JAVA_HOME /usr/lib/jvm/java-8-oracle