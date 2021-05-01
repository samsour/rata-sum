# Rata Sum
> Raspberry Pi Homeserver Configuration named after the Asurian capital in Tyria (Guild Wars).

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg?style=flat-square)](https://opensource.org/licenses/MIT) [![GitHub Last Commit](https://img.shields.io/github/last-commit/samsour/rata-sum?style=flat-square)](https://github.com/samsour/rata-sum)

Services:

- [Homer](https://github.com/bastienwirtz/homer) as service dashboard

- [Home Assistant](https://home-assistant.io), an Home Automation platform

## Requirements

- [Docker](https://docs.docker.com/install/) + [`docker-compose`](https://docs.docker.com/compose/install/)

## Install

```zsh
# clone the repo to your local machine
git clone https://github.com/samsour/rata-sum

# setup secret env variables
cp .env{.example,} && editor .env

# start up services
docker-compose up --detach
```

## Update

To manually update the containers you can use the following commands:

```zsh
# pull image updates
docker-compose pull

# re-create containers
docker-compose up --detach --remove-orphans
```

## Service CLIs

### The `hass` command

```zsh
docker exec -it homeassistant hass -h
```

For more information on the `hass` command itself [visit their docs](https://www.home-assistant.io/docs/tools/hass/).

## License

[MIT](LICENSE.md) – © 2021 [Sam Sauer](https://samsour.de)