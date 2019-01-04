# Friday

## Included Software

- Transmission
- Couchpotato
- Sickchill
- Lidarr
- Emby
- Ombi
- Heimdall
- Nzbget
- Nzbhydra2
- Jackett
- Smokeping

## Requirements

- Docker
- Docker Compose

# Set up

 - Copy the file `.env.example` to `.env` and edit accordingly. The only thing you really need to
care about in this file are the `PGID` and `PUID`. Ensure they are the same as the user you wish to
run the containers as. You may create a user just for this or you can use your own user. You can use
the command `id $(whoami)` to find you user id. Linux boxes usually have `1000` as your UID and
macOS usually `501` (it may vary). For the GID, Linux should work with `1000` and macOS usually is
`20`.

 - Clone this repository, cd into it and run `docker-compose up -d`

 - Add the following to your hosts file:

```
# Friday
127.0.0.1 emby.friday
127.0.0.1 ombi.friday
127.0.0.1 jackett.friday
127.0.0.1 transmission.friday
127.0.0.1 couchpotato.friday
127.0.0.1 sickchill.friday
127.0.0.1 lidarr.friday
127.0.0.1 nzbget.friday
127.0.0.1 hydra.friday
127.0.0.1 heimdall.friday
127.0.0.1 smokeping.friday
```

## Configuring included software

:construction: This area is under construction

 - Heimdall URL: http://heimdall.friday:9876 
 - Transmission URL: http://transmission.friday:9091
 - Nzbget URL: http://nzbget.friday:6789
 - Emby URL: http://emby.friday:8096
 - Couchpotato URL: http://couchpotato.friday:5050
 - Sickchill URL: http://sickchill.friday:8181
 - Ombi URL: http://ombi.friday:3579
 - Lidarr URL: http://lidarr.friday:8686
 - Hydra2 URL: http://hydra.friday:5076
 - Jackett URL: http://jackett.friday:9117
 - Smokeping URL: http://smokeping.friday:9886/smokeping/smokeping.cgi
 
 ## TO-DO
 
 - [ ] Add a TRAEFIK reverse proxy to drop ports on hostnames
 - [ ] Add better monitoring solution (netdata?, prometheus?)
 - [ ] Make a better README

 ---
 