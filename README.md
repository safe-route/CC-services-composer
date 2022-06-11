# Service Composer

Serves as a web app and services one command deployment repository. The main purpose of this repository is to act as a one click option for deploying locally with a series of docker container without any orchestration. 

## Summary

Used as a one-click deploy option for locally deployable resources such as saferoute-jwt-express with the required database, which is simulated in one large network governed by docker default provisioned DNS when using `docker-compose`.

## Reference

Per the statement on docker website regarding [compose](https://docs.docker.com/compose/), which describe the usage which we need to define the `docker-compose.yml`, because the details is just far to broad to put in this README, we suggest you to just read up the docker documentation for more detailed information

## Structure

There are no specific structure in this repository but you need to make sure you put the `docker-compose.yml` on the root of the repository.

## Usage

This is meant for deployment, and testing purposes. Docker is mandatory, so make sure you have one installed in your machine. First get the repositories with `sh get-repositories.sh`, then enter this into your command line `docker compose up` and if you done using it use `docker compose down` to bring down the network, and containers. For more info in how to use the specific resources refer to their individual repository page you can find in `get-respositories.sh`

### Modification

There are no specific place in which you need to append to in order to add a service just to make sure you add it after this line:

```yaml
version: "3.8"

services:
    <define_services_here>
```