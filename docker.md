# docker

## useful commands

### cleaning shit after docker

#### showing how much space docker uses on your machine

```bash
docker system df
```

this will print something like this

```bash
$ docker system df
TYPE            TOTAL     ACTIVE    SIZE      RECLAIMABLE
Images          11        0         4.178GB   4.178GB (100%)
Containers      0         0         0B        0B
Local Volumes   0         0         0B        0B
Build Cache     0         0         0B        0B
```

#### delete unused build cache

```bash
docker builder prune
```

#### delete unused images

```bash
docker image prune
```

#### delete stopped containers

```bash
docker container prune
```

#### delete unused volumes

```bash
docker volume prune
```

#### delete all at once

```bash
docker system prune
```