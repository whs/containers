# PowerDNS

Example compose:

```yaml
version: "2"
services:
  pdns:
    restart: unless-stopped
    image: willwill/pdns
    volumes:
      - pdns:/data/
    ports:
      - 53:53
      - 53:53/udp
volumes:
  pdns: {}
```
