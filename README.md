# Postgres server
 Postgres server for local development


This server is used in few projects, easy to setup and turn on and off


## Start Postgres
Pull the postgres image from hub.docker.com, create a container named "my_postgres", and start it in the background:

``` docker-compose up -d ```

See that it's working

See the logs:

```docker logs -f my_postgres```

Try running psql:

```docker exec -it my_postgres psql -U postgres```

hit *CTRL+D* to exit

For other commands such as starting, stopping, listing or deleting, see my Docker cheat sheet.

## Create a database

```docker exec -it my_postgres psql -U postgres -c "create database my_database"```

## Connect using Python and psycopg2

```
python3.6 -m venv myenv
source myenv/bin/activate
pip install psycopg2-binary
```
### Use the file named myscript.py

## Run it

```
python myscript.py
```

*(1, 100, 'abcdef')*