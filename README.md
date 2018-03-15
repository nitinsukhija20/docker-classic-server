# WowStack: a dockerized Vanilla WoW environment

**WARNING**: this is a work in progress environment and _may_ fail to work.

Running [Vanilla Wow][wow-1] can be quite the drag if compiling and maintaining
a moving Open Source project is not your forté.

Now things are easier. This provides a containerized environment for running
a full environment supporting Vanilla WoW, and allows enjoying a long-gone game
of World of Warcraft using client 1.12.x (in your prefered locale).

## TODO: Work in progress

- [x] Provision and configure MariaDB
- [x] Provision Vanilla WoW authentication server
- [x] Configure authentication server on startup
- [ ] Provision authentication database and content on startup

## Requirements

Since this is all prebuilt and updated by us, all you have to worry about is
having [Docker][docker] and [Docker Compose][docker-compose] installed.

Feel free to use Docker for Mac OS, Docker for Windows or Docker for Linux,
all work the same.

## Usage

First - to reduce initial start times - pull all Docker containers required by
executing:

```bash
docker-compose pull
```

This will retrieve the WowStack containers for map data, the authentication
server, and the game world server. To support this, we will also pull a MariaDB
container to house the game content during runtime.

As with any composed Docker environment, running the Vanilla WoW environment is
simple:

```bash
docker-compose up -d
```

[wow-1]: http://blizzard.com/games/wow/
[docker]: https://docs.docker.com/install/
[docker-compose]: https://docs.docker.com/compose/install/
