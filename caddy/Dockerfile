FROM alpine:3.6

ENV CADDYPATH=/var/www/html/
ARG version=0.10.7

RUN apk add --no-cache ca-certificates tini libressl \
	&& mkdir app \
	&& wget -O - https://github.com/mholt/caddy/releases/download/v${version}/caddy_v${version}_linux_amd64.tar.gz | tar -C /app/ -xvzf - caddy \
	&& chmod +x /app/caddy \
	&& apk del libressl

STOPSIGNAL SIGQUIT

ENTRYPOINT ["/sbin/tini", "--"]
CMD ["/app/caddy", "-conf", "/var/www/html/Caddyfile"]
