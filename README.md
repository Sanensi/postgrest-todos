## Running everything postgres related with docker!

Starting the different services and connecting to the database as postgres.

```bash
docker-compose up -d
docker exec -it todos-db-1 bash
psql -U postgres
```

## Creating a volume for pgAdmin4

pgAdmin4 need write access to the pgadmin and pgadmin4 folder on the host:

```bash
sudo chown -R 5050:5050 pgadmin
sudo chown -R 5050:5050 pgadmin4
```

## Adding a DB connection to pgAdmin

- Host name: `host.docker.internal`
- Username: `postgres`
