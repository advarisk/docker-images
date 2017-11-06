FROM ubuntu:xenial
ENV  LANG=C.UTF-8

RUN sed -i -e "s!# deb-src http://archive.ubuntu.com/ubuntu/!deb-src http://archive.ubuntu.com/ubuntu/!g" /etc/apt/sources.list && \
  apt-get update && apt-get install -y \
    git \
    sudo \
    gnupg2 \
    reprepro \
    build-essential \
    devscripts \
    equivs \
    debian-keyring \
    ruby-dev \
    libffi-dev \
    jq \
    python-setuptools \
    python3-click \
    python3-yaml \
    python3-lxml \
    python3-requests \
    python3-setuptools

RUN gem install fpm --no-ri --no-rdoc

RUN apt-get build-dep -y \
  lxml \
  tesseract \
  openssh
