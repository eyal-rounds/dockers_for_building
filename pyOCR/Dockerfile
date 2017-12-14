FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive
# Install base utilities
RUN apt-get update && apt-get install -y software-properties-common \
        python-software-properties git build-essential unzip python3 python3-pip tesseract-ocr libmagickwand-dev vim tesseract-ocr-heb

RUN pip3 install --upgrade pip
RUN pip3 install git+https://github.com/jflesch/pyocr.git
RUN pip3 install wand
