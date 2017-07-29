# Rainloop Webmail

Example compose:

```yaml
version: '2'
services:
  rainloop:
    image: willwill/rainloop
    restart: unless-stopped
    volumes:
      - rainloop:/var/www/html/data/
volumes:
  rainloop: {}
```
