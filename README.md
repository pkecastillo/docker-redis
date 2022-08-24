## Redis Server container based on latest redis official image version

### Managed for docker-compose YML

- Network mode: host (port standard redis used on anfitrion server)

### Start container

```
git clone https://github.com/pkecastillo/docker-redis.git

cd docker-redis

docker-compose up -d
```

### Other simple option

```
docker run --name redis-master \
-e REDIS_REPLICATION_MODE=master \
-e REDIS_PASSWORD=masterpassword123 \
bitnami/redis:latest
```