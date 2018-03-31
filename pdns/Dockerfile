FROM alpine:edge
ENV PDNS_VERSION=4.1.1-r3
RUN apk add --no-cache pdns pdns-backend-bind
COPY pdns.conf /etc/pdns/pdns.conf
EXPOSE 53
EXPOSE 53/udp
ENTRYPOINT ["/usr/sbin/pdns_server", "--guardian=no", "--daemon=no", "--write-pid=no"]
