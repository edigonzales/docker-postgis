# docker-postgis

PostGIS-Dockerimage mit ogr foreign data wrapper für lokale Entwicklungen. 

## Build

```
docker build -t sogis/postgis: 16-3.4
```

## Run

```
docker run --rm --name editdb -p 54321:5432 -e POSTGRES_PASSWORD=secret -e POSTGRES_DB=edit -e POSTGRES_HOST_AUTH_METHOD=md5 sogis/postgis:16-3.4
```

```
docker run --rm --name editdb -p 54321:5432 -v pgdata:/var/lib/postgresql/data:delegated -e POSTGRES_PASSWORD=secret -e POSTGRES_DB=edit -e POSTGRES_HOST_AUTH_METHOD=md5 sogis/postgis:16-3.4
```