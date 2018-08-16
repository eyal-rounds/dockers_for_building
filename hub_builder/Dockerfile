from ubuntu:latest

RUN DEBIAN_FRONTEND=noninteractive apt-get -yqq update \
 && DEBIAN_FRONTEND=noninteractive apt-get -yqq install openssh-server xorg libgtk2.0-0 default-jre \
    build-essential scons valgrind cmake gcc-multilib ccache quilt libncurses5-dev zlib1g-dev \
    sudo vim curl wget unzip python python-pip gawk flex gettext locales \
    subversion git-core libboost-regex-dev libcurl4-openssl-dev libmosquitto-dev libssl-dev \
    mosquitto-dev libjson-c-dev mc tcpdump \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN locale-gen en_US.UTF-8
ENV LANG='en_US.UTF-8' LANGUAGE='en_US:en' LC_ALL='en_US.UTF-8'

VOLUME /home/build
WORKDIR /home/build
