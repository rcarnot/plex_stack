# plex_home
Plex stack based on servarr products.

# Apps
https://github.com/linuxserver/docker-wireguard
https://github.com/linuxserver/docker-plex
https://github.com/linuxserver/docker-transmission
https://github.com/linuxserver/docker-prowlarr
https://github.com/linuxserver/docker-sonarr
https://github.com/linuxserver/docker-radarr
https://github.com/FlareSolverr/FlareSolverr
https://github.com/linuxserver/docker-overseerr

# For information 
My stack is managed by portainer. In order to be able to import my conf folder from github and keep them dynamic, I need to map the container /data with the same path (aka. /data) on my local.  
eg.
'' 
version: "3.9"
services:
  portainer:
    image: portainer/portainer-ce:latest
    container_name: portainer
    volumes:
      - /data:/data
      - /var/run/docker.sock:/var/run/docker.sock
    ports:
      - 8000:8000
      - 9000:9000
    restart: unless-stopped
''