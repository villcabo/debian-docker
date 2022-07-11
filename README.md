# debian-docker
Debian Docker


# Docker Debian Server

This image is based on **debian**

Build image with default arguments:
```
docker compose build --force-rm
```

Build image with custom arguments:
```
docker compose build --force-rm --build-arg USER=debian --build-arg PASS=debian
```

Start container:
```
docker compose up -d
```

Start container with build:
```
docker compose up -d --build
```

Destroy container:
```
docker compose down
```