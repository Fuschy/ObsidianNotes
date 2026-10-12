```YAML
services:

  tautulli:

    image: linuxserver/tautulli:latest

    container_name: tautulli

    environment:

      - PUID=1028 #CHANGE_TO_YOUR_UID

      - PGID=65536 #CHANGE_TO_YOUR_GID

      - TZ=Europe/Berlin #CHANGE_TO_YOUR_TZ

      - UMASK=022

    volumes:

      - /volume1/docker/tautulli:/config

    ports:

      - 8181:8181/tcp

    network_mode: synobridge

    security_opt:

      - no-new-privileges:true

    restart: always
```