from ubuntu:latest

MAINTAINER eyalrounds

ENV LANG='en_US.UTF-8' LANGUAGE='en_US:en' LC_ALL='en_US.UTF-8'

RUN DEBIAN_FRONTEND=noninteractive apt-get -yqq update \
 && DEBIAN_FRONTEND=noninteractive apt-get -yqq install \
	gawk wget git-core diffstat unzip texinfo gcc-multilib build-essential \
	chrpath socat cpio python python3 python3-pip python3-pexpect \
	xz-utils debianutils iputils-ping valgrind cmake vim curl \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

RUN git clone git://git.yoctoproject.org/poky -b thud
WORKDIR ./poky
RUN bash -c "source oe-init-build-env" 


