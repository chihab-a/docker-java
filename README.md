# docker-java
Personal Java docker image based on Debian 9 (Stretch)

# Java 8 (1.8.0_111)
----
### Pull from Docker Hub
```
docker pull glob-dev/java:latest
```

### Build from GitHub
```
docker build -t glob-dev/java github.com/glob-dev/docker-java
```

### Run image
```
docker run -it glob-dev/java bash
```

### Use as base image
```Dockerfile
FROM glob-dev/java:latest
```
