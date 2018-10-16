[![Docker Stars](https://img.shields.io/docker/stars/sunx/alpine-glibc.svg?style=flat-square)](https://hub.docker.com/r/sunx/alpine-glibc/)
[![Docker Pulls](https://img.shields.io/docker/pulls/sunx/alpine-glibc.svg?style=flat-square)](https://hub.docker.com/r/sunx/alpine-glibc/)

Docker image of Alpine Linux with GNU C library (glibc)
========================================================

This image is based on Alpine Linux image (smallest linux image if not count busybox image) with added glibc to add ability to run some applications, which requre glibc ( for example OpenJDK and different proprietary applications).

Download size of this image is only:

[![](https://images.microbadger.com/badges/image/sunx/alpine-glibc.svg)](http://microbadger.com/images/sunx/alpine-glibc)


Different architectures and versions
-------------------------------------

This image is build with latest Alpine Linux image and glibc 2.28 and available for amd64 architecture (most modern desktops/laptops). Also most applications, distributed with glibc are deleted from image to save space (they usually not needed in docker images anyway). If you need image with different version of Apline Linux or glibc, or for different architecture, you can download original [Dockerfile](https://github.com/VGoshev/alpine-glibc/blob/master/Dockerfile), edit glibc/Alpine version and build for preferred architecture, tested to work properly on ARM64 and ARM32 architectires.

Usage Example
-------------

This image is intended to be a base image for your projects, so you may use it like this:

```Dockerfile
FROM sunx/alpine-glibc

COPY ./app /usr/local/bin/my_app
CMD /usr/local/bin/app
```

```sh
$ docker build -t my_app .
```
