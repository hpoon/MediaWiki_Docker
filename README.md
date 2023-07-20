Building on top of the mediawiki Docker image and then adding the ability to run it with different user ID and group ID

Usage:

```
wiki:
    image: henrypoon/mediawiki
    restart: unless-stopped
    volumes:
      - path-to-images:/var/www/html/images
      - path-to-data:/var/www/data
      - path-to-LocalSettings.php:/var/www/html/LocalSettings.php:ro
    environment:
      - PUID=1001
      - PGID=998
```
