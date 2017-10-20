Docker Java 9
============

## Summary

Repository name in Docker Hub: **[globdev/java](https://registry.hub.docker.com/u/globdev/java/)**

This repository contains Dockerized [Java](https://www.java.com/) 1.9, published to the public [Docker Hub](https://registry.hub.docker.com/) via **automated build** mechanism.

## Configuration

This docker image contains the following software stack:

- OS: Debian stretch (built from [debian:stretch](https://registry.hub.docker.com/_/debian/)).

- Java: Oracle JDK 9.0.1+11

### Dependencies

- [debian:stretch](https://registry.hub.docker.com/_/debian/).


## Installation

   ```
   $ docker pull globdev/java:9
   ```

## Usage

#### Use as base image

```Dockerfile
FROM globdev/java:9
```

#### Pull from Docker Hub

```
docker pull globdev/java:9
```

#### Build from GitHub

```
docker build -t globdev/java:9 github.com/glob-dev/docker-java/java-9
```

#### Run image

```
docker run -it globdev/java:9 bash
```

#### Run `java`

```
$ docker run --rm globdev/java:9
```

#### Run `javac`

```
$ docker run -it --rm globdev/java:9 javac
```