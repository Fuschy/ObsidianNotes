```YAML
services:

  sabnzbd:

    image: linuxserver/sabnzbd:latest

    container_name: sabnzbd

    environment:

      - PUID=1028 #CHANGE_TO_YOUR_UID

      - PGID=65536 #CHANGE_TO_YOUR_GID

      - TZ=Europe/Berlin #CHANGE_TO_YOUR_TZ

      - UMASK=022

    volumes:

      - /volume1/docker/sabnzbd:/config

      - /volume1/data/usenet:/data/usenet

      - /volume1/PC-Share:/data/PC-Share

    ports:

      - 8080:8080/tcp

    network_mode: synobridge

    security_opt:

      - no-new-privileges:true

    restart: always
```