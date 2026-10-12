```YAML
services:

  jellyseerr:

    image: fallenbagel/jellyseerr:latest

    container_name: jellyseerr

    user: 1028:65536 #YOUR_UID_AND_GID

    environment:

      - TZ=Europe/Berlin #CHANGE_TO_YOUR_TZ

    volumes:

      - /volume1/docker/jellyseerr:/app/config

    ports:

      - 5055:5055/tcp

    network_mode: synobridge

    dns: #DNS Servers to help with speed issues some have

      - 9.9.9.9

      - 1.1.1.1

    security_opt:

      - no-new-privileges:true

    restart: always
```