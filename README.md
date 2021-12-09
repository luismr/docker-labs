# docker-labs

## Requirements

The tests used these builds/versions

* Docker version 20.10.10, build b485636
* docker-compose version 1.29.2, build 5becea4c

## Stacks

### postgres-php7

#### Containers

* web (PHP7-Apache + Postgres Client Support)
* db (Postgres)

#### Code

Please place your code at

```shell
postgres-php7/src
```

#### Building

```shell
cd postgres-php7
docker-compose pull
docker-compose build
docker-compose up -d
```

#### Run

You can access your PHP scripts at

```shell
https://localhost/<script_file_name>.php
```

### postgres-db

#### Containers

* db-admin (PGAdmin 4)
* db (Postgres)

#### Building

```shell
cd postgres-db
docker-compose pull
docker-compose build
docker-compose up -d
```

#### Run

##### db-admin

```shell
https://localhost:5433/
```

##### db

```
hostname ..: localhost
port ......: 5432
username ..: postgres
password ..: devdev
```