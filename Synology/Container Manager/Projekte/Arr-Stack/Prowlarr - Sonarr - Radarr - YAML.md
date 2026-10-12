```YAML
services:

  sonarr:

    image: linuxserver/sonarr:latest

    container_name: sonarr

    environment:

      - PUID=1028 #CHANGE_TO_YOUR_UID

      - PGID=65536 #CHANGE_TO_YOUR_GID

      - TZ=Europe/Berlin #CHANGE_TO_YOUR_TZ

      - UMASK=022

    volumes:

      - /volume1/docker/sonarr:/config

      - /volume1/data:/data

    ports:

      - 8989:8989/tcp

    network_mode: synobridge

    security_opt:

      - no-new-privileges:true

    restart: always

  radarr:

    image: linuxserver/radarr:latest

    container_name: radarr

    environment:

      - PUID=1028 #CHANGE_TO_YOUR_UID

      - PGID=65536 #CHANGE_TO_YOUR_GID

      - TZ=Europe/Berlin #CHANGE_TO_YOUR_TZ

      - UMASK=022

    volumes:

      - /volume1/docker/radarr:/config

      - /volume1/data:/data

    ports:

      - 7878:7878/tcp

    network_mode: synobridge

    security_opt:

      - no-new-privileges:true

    restart: always

  

  prowlarr:

    image: linuxserver/prowlarr:latest

    container_name: prowlarr

    environment:

      - PUID=1028 #CHANGE_TO_YOUR_UID

      - PGID=65536 #CHANGE_TO_YOUR_GID

      - TZ=Europe/Berlin #CHANGE_TO_YOUR_TZ

      - UMASK=022

    volumes:

      - /volume1/docker/prowlarr:/config

    ports:

      - 9696:9696/tcp

    network_mode: synobridge

    security_opt:

      - no-new-privileges:true

    restart: always
```
