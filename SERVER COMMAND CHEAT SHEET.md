# Server Command Cheat Sheet

Enter The server

```
ssh developer@13.236.149.81
```

### See all the running docker application

```
docker ps -a
```

Example
```
CONTAINER ID   IMAGE                     COMMAND                  CREATED          STATUS          PORTS                                                   NAMES
f12237e3abae   rentyard/dl-backend:32    "docker-entrypoint.s…"   36 minutes ago   Up 36 minutes   0.0.0.0:7777->7777/tcp, [::]:7777->7777/tcp             dl-backend
915355419bc8   rentyard/dl-frontend:30   "entrypoint.sh node …"   23 hours ago     Up 23 hours     3000/tcp, 0.0.0.0:3100->3100/tcp, [::]:3100->3100/tcp   dl-frontend
```

- NAMES,CONTAINER ID is important here

### See Logs

```
docker logs <container id/name> -f --tail 400
```

### See container meta data

```
docker inspect <container id/name>
```

### docker application restart

```
docker restart <container id/name>
```

### dokcer application stop

```
docker stop <container id/name>
```

### Docker application pull and start (This will be needed for production server)

```
TAG=12 docker compose pull && docker compose up -d
```

- here TAG number will be github action run number.
##### Example
