FROM ubuntu:18.04

ENV DEBIAN_FRONTEND=noninteractive
WORKDIR /root

# Use OSU OSL for package mirror!
RUN \
sed -i 's@http://archive.ubuntu.com/ubuntu/@http://ubuntu.osuosl.org/ubuntu@g' /etc/apt/sources.list && \
apt-get -qq update && \
apt-get -yqq install nano nmap htop curl wget inetutils-ping dnsutils software-properties-common telnet tcpdump

RUN \
apt-add-repository -y ppa:git-core && \
apt-get -qq update && \
apt-get install -yqq git && \
apt-get clean && \
rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*