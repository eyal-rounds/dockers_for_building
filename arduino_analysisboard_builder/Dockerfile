FROM ubuntu:17.10

RUN apt-get update \
	&& apt-get install -y \
	   wget \
	   openjdk-9-jre \
	   xvfb \
	   xz-utils \
	&& apt-get clean \
	&& rm -rf /var/lib/apt/lists/*

ENV ARDUINO_IDE_VERSION 1.8.5
RUN (wget -q -O- https://downloads.arduino.cc/arduino-${ARDUINO_IDE_VERSION}-linux64.tar.xz \
	| tar xJC /usr/local/share \
	&& ln -s /usr/local/share/arduino-${ARDUINO_IDE_VERSION} /usr/local/share/arduino \
	&& ln -s /usr/local/share/arduino-${ARDUINO_IDE_VERSION}/arduino /usr/local/bin/arduino)

COPY ./start-xvfb.sh /usr/local/bin/start-xvfb

ENV DISPLAY :1.0

COPY ./start-session.sh /usr/local/bin/start-session

RUN arduino --install-boards "arduino:samd"

RUN echo "boardsmanager.additional.urls=https://adafruit.github.io/arduino-board-index/package_adafruit_index.json" >> /root/.arduino15/preferences.txt

RUN arduino --install-boards "adafruit:samd"

CMD ["/bin/bash"]
