FROM alpine:3.6

ENV CADDYPATH=/var/www/html/
ARG version=0.10.9-w

RUN apk add --no-cache ca-certificates tini libressl \
	&& mkdir app \
	&& wget -O /app/wedge https://github.com/WedgeServer/wedge/releases/download/v${version}/wedge_linux_amd64 \
	&& chmod +x /app/wedge \
	&& apk del libressl

STOPSIGNAL SIGQUIT

ENTRYPOINT ["/sbin/tini", "--"]
CMD ["/app/wedge", "-conf", "/var/www/html/Wedgefile"]
