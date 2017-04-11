FROM alpine:edge

ARG github_token

WORKDIR /root

COPY rancher-cli-download.sh .

RUN \
apk --update --no-cache add curl jq openssl && \
/root/rancher-cli-download.sh && \
tar xvf rancher-linux-amd64* && \
cp rancher-v*/rancher /usr/local/bin && \
apk del jq openssl && \
rm -rf rancher* /var/cache/apk/* /var/cache/misc/*

CMD ["/bin/ash"]
