# docker-compose-i386-transmission
A simple docker-compose YML for quickly running on i368 transmission

```
version: "3"
services:
  transmission:
    container_name: transmission
    image: jaymoulin/transmission
    environment:
      - PUID=1000
      - PGID=1001
      - TZ=America/Guayaquil
      #- USERNAME=username
      #- PASSWORD=password
# default username and password "" ""
    ports:
      - 9091:9091
    restart: unless-stopped
    volumes:
      - <path to config>:/config
      - <path to downloads>:/output
```
