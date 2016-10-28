FROM ubuntu:16.04

MAINTAINER "Chris Mosetick" <cmosetick@gmail.com>

ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /root

# Use OSU OSL for package mirror!
RUN \
sed -i 's@http://archive.ubuntu.com/ubuntu/@http://ubuntu.osuosl.org/ubuntu@g' /etc/apt/sources.list && \
apt-get -qq update && \
apt-get -yqq install git nano nmap htop inetutils-ping software-properties-common man

RUN \
apt-add-repository -y ppa:git-core && \
apt-get -qq update && \
apt-get install -yqq git && \
apt-get clean && \
rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
