# docker-labs

## Requirements

The tests used these builds/versions

* Docker version 20.10.10, build b485636
* docker-compose version 1.29.2, build 5becea4c

## Stacks

### Postgres

#### Containers

* web (PHP7-Apache + Postgres Client Support)
* db (Postgres)

#### Run

```shell
cd postgres
docker-compose pull
docker-compose build
docker-compose up -d
```