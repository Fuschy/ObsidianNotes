```YAML
version: '3'

services:

  makemkv:

    image: jlesage/makemkv

    ports:

      - "5800:5800"

    volumes:

      - "/volume1/docker/makemkv:/config:rw"

      - "/volume1/docker/makemkv:/storage:ro"

      - "/volume1/docker/makemkv/data:/output:rw"

    devices:

      - "/dev/sg5:/dev/sg5"
```