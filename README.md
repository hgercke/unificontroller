# Docker Ubiquiti UniFi controller

This builds a Docker Image of the Ubiquiti UniFi Controller.

## About

This project is basically a clone of https://github.com/jasonbronson/ubiquiti-controller
But is has been updated to use Ubiquiti package repo and newer version of Ubuntu as baseimage. The Unifi-controller
has been updated to version 6.2.26


# Ports exposed

- 3478/udp
- 8080
- 8443
- 8880
- 8843
- 6789
- 5656-5699/udp
- 10001/udp
- 1900/udp


## How to build

```
 git clone https://github.com/hgercke/unificontroller.git
 cd unificontroller/docker
 docker build -t unificontroller:6.2.26 .
```

## How to run example

```
  docker run -d --restart=always -p 8080:8080 -p8443:8443 -v /myhost/unifidb:/var/lib/unifi/db unificontroller:6.2.26
```
