# Gnosis Database Service

Simple implementation of MySQL Service. <br> 
This repository is used to simply set the environment variables and use the docker-compose file to easily deploy a MySQL RDBMS service for [gnosis_main_service](https://github.com/damsog/gnosis-main-service) although it can be used for any application.

For more information about the face recognition application refer to : [gnosis_main_service](https://github.com/damsog/gnosis-main-service)

## :clipboard: Requirements
##### :penguin: Dependencies
- [Docker](https://docs.docker.com/engine/install/ubuntu/)

### :whale2: *Run as Container*

Before deploying the service you have to set up the environment variables. create a file called .env and copy the content from .base.env
```sh
cp .base.env .env
```
Let's explain the parameters to set on the .env file. <br>
Set the database name. then, set the access cretentials for the service, user, password, host and then the port tor run on.
```
DB_NAME=<dbname>
DB_USER=<user>
DB_PASS=<pass>
DB_HOST=<host>
DB_PORT=<port>
```

Run Docker container. deploy using the docker compose file
To run using docker compose
```sh
docker compose up
```
or in detatched mode
```sh
docker compose up -d
```
to stop 
```sh
docker compose down
```

Check outputs 
```sh
docker logs --tail N <container_id>
```