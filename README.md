# Postgres server
 Postgres server for local development


This server is can be used in dev projects, easy to setup and turn on and off. This version saves data to volume, so you can turn it off when needed without losing your data.


## Start Postgres
Pull the postgres image from hub.docker.com, create a container named "my_postgres", and start it in the background:

``` docker-compose up -d ```

Credentials are in docker-compose.yml

Port to connect is also in there.

## This is not necessary
See that it's working

See the logs:

```docker logs -f my_postgres```

Try running psql:

```docker exec -it my_postgres psql -U postgres```

hit *CTRL+D* to exit

For other commands such as starting, stopping, listing or deleting, see my Docker cheat sheet.

## Create a new database

```docker exec -it my_postgres psql -U postgres -c "create database my_database"```
