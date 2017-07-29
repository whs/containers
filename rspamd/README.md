# rspamd

Example compose:

```yaml
version: '2'
services:
  rspamd:
    image: willwill/rspamd
    restart: unless-stopped
    volumes:
      - rspamd:/etc/rspamd
volumes:
  rspamd: {}
```
