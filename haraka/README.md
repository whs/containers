# Haraka

Example compose:

```yaml
version: '2'
services:
  smtp:
    image: willwill/haraka
    restart: unless-stopped
    volumes:
      - haraka:/data
      - certs:/certs:ro,z
    ports:
      - "25:25"
      - "587:587"
volumes:
  haraka: {}
  certs:
    external: true
```

Note: certs is [acme-docker](https://hub.docker.com/r/willwill/acme-docker/)'s state volume.
