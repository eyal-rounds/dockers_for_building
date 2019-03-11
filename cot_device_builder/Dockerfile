from ubuntu:latest

MAINTAINER eyalrounds

ENV LANG='en_US.UTF-8' LANGUAGE='en_US:en' LC_ALL='en_US.UTF-8'

RUN DEBIAN_FRONTEND=noninteractive apt-get -yqq update \
 && DEBIAN_FRONTEND=noninteractive apt-get -yqq install \
    build-essential scons valgrind cmake gcc-multilib ccache quilt libncurses5-dev zlib1g-dev libssl-dev \
    vim curl wget unzip python3 python3-pip gawk flex gettext libcurl4-openssl-dev libmosquitto-dev \
    mosquitto-dev libjson-c-dev git-core \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN mkdir /etc/cloudofthings/

