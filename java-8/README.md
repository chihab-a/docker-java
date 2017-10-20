Docker Java 8
============

#### Summary

Repository name in Docker Hub: **[globdev/java](https://registry.hub.docker.com/u/williamyeh/java8/)**

This repository contains Dockerized [Java](https://www.java.com/) 1.8, published to the public [Docker Hub](https://registry.hub.docker.com/) via **automated build** mechanism.

#### Configuration

This docker image contains the following software stack:

- OS: Debian stretch (built from [debian:stretch](https://registry.hub.docker.com/_/debian/)).

- Java: Oracle JDK 1.8.0_151-b12


#### Dependencies

- [debian:stretch](https://registry.hub.docker.com/_/debian/).


#### Installation

   ```
   $ docker pull globdev/java:8
   ```

#### Usage

##### Use as base image

```Dockerfile
FROM globdev/java:8
```

##### Pull from Docker Hub

```
docker pull globdev/java:8
```

##### Build from GitHub

```
docker build -t globdev/java:8 github.com/glob-dev/docker-java/java-8
```

##### Run image

```
docker run -it globdev/java:8 bash
```

##### Run `java`

```
$ docker run --rm globdev/java:8
```

##### Run `javac`

```
$ docker run -it --rm globdev/java:8 javac
```