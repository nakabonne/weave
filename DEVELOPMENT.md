# Developer guide

## Build all docker images

Ref: https://www.weave.works/docs/net/latest/building/#building-directly-on-your-machine

Build image to build weave images

```
make .build.uptodate
```

Build all images

```
make
```

Push them to Dockerhub

```
TAG="latest"
docker image tag nakabonne/weave:latest nakabonne/weave:$TAG
docker image push nakabonne/weave:$TAG

docker image tag nakabonne/weaveexec:latest nakabonne/weaveexec:$TAG
docker image push nakabonne/weaveexec:$TAG

docker image tag nakabonne/weavedb:latest nakabonne/weavedb:$TAG
docker image push nakabonne/weavedb:$TAG

docker image tag nakabonne/weave-npc:latest nakabonne/weave-npc:$TAG
docker image push nakabonne/weave-npc:$TAG
```

## Build only weaver image

Build binary

```
make prog/weaver/weaver
```

Generate Dockerfile for Weaver

```
make prog/weaver/Dockerfile.nakabonne
```

Build an image for Weaver

```
make .weaver.uptodate
```
