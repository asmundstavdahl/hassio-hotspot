ARG BUILD_FROM
FROM $BUILD_FROM

MAINTAINER Jaime Quiroga <git@NeodomoEwe.com>

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

ENV LANG C.UTF-8

RUN apk update && \
apk add --no-cache bash jq iw hostapd networkmanager net-tools sudo dnsmasq && \
rm -rf /var/cache/apk/*

COPY hostapd.conf /
COPY dnsmasq.conf /

CMD [ "/bin/bash", "/etc/services.d/hassio-hotspot/run" ]
