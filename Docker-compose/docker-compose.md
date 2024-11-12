# Docker-compose

## Principles

* Docker-compose is a docker plugin for defining multi-container applications.
* It requires configuration file in a yaml format.
* In docker-compose configuration files, it is possible to configure three main things: services; networks and volumes.

## Main commands

* `docker-compose up` :This command is used to run a docker-compose.
* `docker-compose -f <file-path> up` :This command is used to run a docker-compose from a file located in a specific path.
* `docker-compose -d up` :This command is used to run a docker-compose as a daemon.

## Good practices and tips

* Installing docker-compsoe on Debian Linux : `sudo apt-get install docker-compose-plugin` or `curl -SL https://github.com/docker/compose/releases/download/v2.30.3/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose` `chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose`
* [Go to the docker-compose documentation](https://docs.docker.com/compose/)
