# Friday

## Included Software

- Bazarr
- Emby
- Flaresolverr
- Grocy
- Home Assistant
- Homepage
- Lidarr
- Myspeed
- Netdata
- Ombi
- Prowlarr
- Qbittorrent
- Radarr
- Recyclarr
- Sonarr
- Traefik
- Uptime-kuma

## Requirements

- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

# Set up

 - Clone this repository, cd into it.
 - Copy the file `.env.example` to `.env` and edit accordingly.
 - The only thing you really need to care about in the `.env` file are the `PGID`, `PUID` and the MEDIA FOLDERS config block. Ensure they are the same as the user you wish to run the containers as. You may create a user just for this or you can use your own user. You can use the command `id $(whoami)` to find you user id. Linux boxes usually have `1000` as your UID and macOS usually `501` (it may vary). For the GID, Linux should work with `1000` and macOS usually is `20`.
 - Run `docker-compose up -d`
 - Add the following to your hosts file:

```
# Friday
127.0.0.1 bazarr.friday
127.0.0.1 emby.friday
127.0.0.1 flaresolverr.friday
127.0.0.1 grocy.friday
127.0.0.1 homeassistant.friday
127.0.0.1 homepage.friday
127.0.0.1 lidarr.friday
127.0.0.1 myspeed.friday
127.0.0.1 netdata.friday
127.0.0.1 ombi.friday
127.0.0.1 qbittorrent.friday
127.0.0.1 radarr.friday
127.0.0.1 sonarr.friday
127.0.0.1 transmission.friday
```

## URLs

### Hosts files

:construction: This area is under construction

 - Ombi URL: http://ombi.friday:3579
 - Emby URL: http://emby.friday:8096
 - Sonarr URL: http://sickchill.friday:8989
 - Radarr URL: http://radarr.friday:7878
 - Lidarr URL: http://lidarr.friday:8686
 - Flaresolverr URL: http://flaresolverr.friday:8191

### Traefik (replace the domain with your own)

:construction: This area is under construction

 - Ombi URL: https://ombi.local.bizarro.tech
 - Emby URL: https://emby.local.bizarro.tech
 - Sonarr URL: https://sonarr.local.bizarro.tech
 - Radarr URL: https://radarr.local.bizarro.tech
 - Lidarr URL: https://lidarr.local.bizarro.tech

 ## TO-DO

 - [x] Add TRAEFIK as reverse proxy to drop ports on hostnames
 - [ ] Add better monitoring solution (netdata?, prometheus+grafana?)
 - [ ] Make a better README

 ---

 [![forthebadge](https://forthebadge.com/images/badges/contains-cat-gifs.svg)](https://forthebadge.com)
 [![forthebadge](https://forthebadge.com/images/badges/powered-by-netflix.svg)](https://forthebadge.com)

