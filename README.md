# docker-postgis

PostGIS-Dockerimage mit [ogr foreign data wrapper](https://github.com/pramsey/pgsql-ogr-fdw) für lokale Entwicklungen. Für GRETL- und Schema-Jobs nicht zu verwenden!

## Build

```
docker build -t sogis/postgis:16-3.4 .
```

## Run

```
docker run --rm --name editdb -p 54321:5432 -e POSTGRES_PASSWORD=secret -e POSTGRES_DB=edit sogis/postgis:16-3.4
```

```
docker run --rm --name editdb -p 54321:5432 -v pgdata:/var/lib/postgresql/data:delegated -e POSTGRES_PASSWORD=secret -e POSTGRES_DB=edit sogis/postgis:16-3.4
```
