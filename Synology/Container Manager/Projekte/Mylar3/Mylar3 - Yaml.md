```yaml
version: "2.1"

services:

  mylar3:

    image: lscr.io/linuxserver/mylar3:latest

    container_name: mylar3

    environment:

      - PUID=1028

      - PGID=65536

      - TZ=Europe/Berlin

    volumes:

      - /volume1/docker/mylar3/config:/config

      - /volume1/docker/mylar3/comics:/comics

      - /volume1/docker/mylar3/downloads:/downloads

    network_mode: synobridge

    ports:

      - 8090:8090

    restart: unless-stopped
```
