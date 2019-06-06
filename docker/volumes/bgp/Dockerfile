# Quagga OSPF
#
# VERSION 0.0.2

FROM alpine:latest

LABEL maintainer.name="Machado - Blanco" \
      version="0.0.1" \
      description="OSPF + BGP (Alpine + Apache)"

RUN apk update
RUN apk add supervisor quagga heimdal tcpdump

RUN echo "bgpd=yes" >> /etc/quagga/daemons
RUN echo "ospfd=yes" >> /etc/quagga/daemons
RUN echo "zebra=yes" >> /etc/quagga/daemons

ENTRYPOINT ["/usr/bin/supervisord"]
