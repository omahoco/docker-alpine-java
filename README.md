## Minified Docker image with Java 8 and Python 2.7

A basic [Docker](https://www.docker.com/) image to run [Java](https://www.java.com/) and [Python](https://www.python.org) applications.  

This image is:
- A fork of [anapsix/alpine-java](https://hub.docker.com/r/anapsix/alpine-java) using newer Java and glibc versions.
- Based on [python/2.7.14-alpine3.6](https://github.com/docker-library/python/blob/1d59eb2dd813c64891bf554a8ea01754aba25816/2.7/alpine3.6/Dockerfile)

## Why?

Because I needed to create a fat container to run multiple Java processes that are supervised by a python script.

## Details

- Installs 'Oracle JDK 1.8.0_151-b12'
- Installs 'Python 2.7.14'
- Installs 'glibc-2.26'
- Installs 'bash'
- Installs 'curl'

## Build
```shell
docker build 8/current/jdk/unlimited/ -t omahoco1/alpine-java-python
```

## Usage

Start a Python interpreter
```shell
docker run --rm -it omahoco1/alpine-java-python python
```

Run Java
```shell
docker run --rm omahoco1/alpine-java-python java -version
```
