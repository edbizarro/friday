# Friday

## Included Software

- Transmission
- Sonarr
- Lidarr
- Radarr
- Emby
- Ombi
- Heimdall
- Nzbget
- Jackett
- Flaresolverr

## Requirements

- [Docker](https://docs.docker.com/install/)
- [Docker Compose](https://docs.docker.com/compose/install/)

# Set up

 - Clone this repository, cd into it.
 - Copy the file `.env.example` to `.env` and edit accordingly. 
 - The only thing you really need to care about in the `.env` file are the `PGID`,  `PUID` and the MEDIA FOLDERS config block. Ensure they are the same as the user you wish to run the containers as. You may create a user just for this or you can use your own user. You can use the command `id $(whoami)` to find you user id. Linux boxes usually have `1000` as your UID and macOS usually `501` (it may vary). For the GID, Linux should work with `1000` and macOS usually is `20`.
 - Run `docker-compose up -d`
 - Add the following to your hosts file:

```
# Friday
127.0.0.1 heimdall.friday
127.0.0.1 emby.friday
127.0.0.1 sonarr.friday
127.0.0.1 lidarr.friday
127.0.0.1 radarr.friday
127.0.0.1 ombi.friday
127.0.0.1 jackett.friday
127.0.0.1 flaresolverr.friday
127.0.0.1 transmission.friday
127.0.0.1 nzbget.friday
127.0.0.1 hydra.friday
```

## URLs

:construction: This area is under construction

 - Heimdall URL: http://heimdall.friday:9876
 - Ombi URL: http://ombi.friday:3579
 - Transmission URL: http://transmission.friday:9091
 - Emby URL: http://emby.friday:8096
 - Sonarr URL: http://sickchill.friday:8989
 - Radarr URL: http://radarr.friday:7878
 - Lidarr URL: http://lidarr.friday:8686
 - Jackett URL: http://jackett.friday:9117
 - Hydra2 URL: http://hydra.friday:5076
 - Nzbget URL: http://nzbget.friday:6789 
 - Flaresolverr URL: http://flaresolverr.friday:8191
 
 ## TO-DO
 
 - [ ] Add TRAEFIK as reverse proxy to drop ports on hostnames
 - [ ] Add better monitoring solution (netdata?, prometheus?)
 - [ ] Make a better README

 ---
 
 [![forthebadge](https://forthebadge.com/images/badges/contains-cat-gifs.svg)](https://forthebadge.com)
 [![forthebadge](https://forthebadge.com/images/badges/powered-by-netflix.svg)](https://forthebadge.com)
 
