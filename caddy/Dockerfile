FROM alpine:3.6

ENV CADDYPATH=/var/www/html/

RUN apk add --no-cache ca-certificates tini

ADD https://github.com/mholt/caddy/releases/download/v0.10.6/caddy_v0.10.6_linux_amd64.tar.gz /app/

STOPSIGNAL SIGQUIT

ENTRYPOINT ["/sbin/tini", "--"]
CMD ["/app/caddy", "-conf", "/var/www/html/Caddyfile"]
