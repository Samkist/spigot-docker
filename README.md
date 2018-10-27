# Spigot Docker

*Lightweight Minecraft Spigot 1.13.2 server container*

[![Spigot Docker](https://github.com/qdm12/spigot-docker/raw/master/readme/title.png)](https://hub.docker.com/r/qmcgaw/spigot)

[![Build Status](https://travis-ci.org/qdm12/spigot-docker.svg?branch=master)](https://travis-ci.org/qdm12/spigot-docker)
[![Docker Build Status](https://img.shields.io/docker/build/qmcgaw/spigot.svg)](https://hub.docker.com/r/qmcgaw/spigot)

[![GitHub last commit](https://img.shields.io/github/last-commit/qdm12/spigot-docker.svg)](https://github.com/qdm12/spigot-docker/issues)
[![GitHub commit activity](https://img.shields.io/github/commit-activity/y/qdm12/spigot-docker.svg)](https://github.com/qdm12/spigot-docker/issues)
[![GitHub issues](https://img.shields.io/github/issues/qdm12/spigot-docker.svg)](https://github.com/qdm12/spigot-docker/issues)

[![Docker Pulls](https://img.shields.io/docker/pulls/qmcgaw/spigot.svg)](https://hub.docker.com/r/qmcgaw/spigot)
[![Docker Stars](https://img.shields.io/docker/stars/qmcgaw/spigot.svg)](https://hub.docker.com/r/qmcgaw/spigot)
[![Docker Automated](https://img.shields.io/docker/automated/qmcgaw/spigot.svg)](https://hub.docker.com/r/qmcgaw/spigot)

[![Image size](https://images.microbadger.com/badges/image/qmcgaw/spigot.svg)](https://microbadger.com/images/qmcgaw/spigot)
[![Image version](https://images.microbadger.com/badges/version/qmcgaw/spigot.svg)](https://microbadger.com/images/qmcgaw/spigot)

| Download size | Image size | RAM usage | CPU usage |
| --- | --- | --- | --- |
| ?MB | 132MB | 300MB | Medium |

Based on:

- Alpine Linux 3.8
- OpenJDK JRE 8

## Setup

[![Spigot](https://github.com/qdm12/spigot-docker/raw/master/readme/spigot.png)](https://www.spigotmc.org)

### Server launch

```bash
docker run -d --name=spigot -p 25565:25565/tcp \
-v './spigot:/spigot' -e ACCEPT_EULA=true qmcgaw/spigot
```

or with `docker-compose up -d` using the [docker-compose.yml](https://github.com/qdm12/spigot-docker/raw/master/docker-compose.yml) file.

The environment variable `ACCEPT_EULA` is used to accept the SpigotMC EULA license (required to run the server).

If you have existing server data, simply place it in `./spigot` then launch the container as described above.

## TODOs

- Execute commands in server
- Stop server gracefully
- Healthcheck
- Stop procedure
- Plugins

I recommend using the [Hibernate plugin](https://www.spigotmc.org/resources/hibernate.4441/) for your Spigot Docker server

[![Hibernate plugin](readme/hibernate.png)](https://www.spigotmc.org/resources/hibernate.4441/)
