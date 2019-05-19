FROM majid7221/debian:stretch

RUN set -ex \
    && apt-key adv --no-tty --keyserver hkp://keyserver.ubuntu.com:80 --recv-keys EA8CACC073C3DB2A \
    && echo "deb http://ppa.launchpad.net/linuxuprising/java/ubuntu bionic main" | tee /etc/apt/sources.list.d/linuxuprising-java.list \
    && echo oracle-java11-installer shared/accepted-oracle-license-v1-2 select true | /usr/bin/debconf-set-selections \
    && mkdir /usr/share/man/man1 \
    && apt-get update \
    && apt-get install -y oracle-java11-installer \
    && java -version \
    && rm -rf /var/lib/{apt,dpkg,cache,log}/ /tmp/* /var/tmp/*

ENV JAVA_HOME /usr/lib/jvm/java-11-oracle