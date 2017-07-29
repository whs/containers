# Dovecot

Example compose:

```yaml
version: '2'
services:
  imap:
    image: willwill/dovecot
    restart: unless-stopped
    volumes:
      - dovecot:/etc/dovecot
      - certs:/etc/certs:ro,z
      - mailbox:/var/vpopmail/
    ports:
      - 143:143 # imap
      - 993:993 # imaps
      - 110:110 # pop3
      - 995:995 # pop3s
volumes:
  dovecot: {}
  mailbox: {}
  certs:
    external: true
```

Note: certs is [acme-docker](https://hub.docker.com/r/willwill/acme-docker/)'s state volume.

This image have hard coded certificate file name, so you probably need to edit /etc/dovecot/conf.d/91-docker.conf
