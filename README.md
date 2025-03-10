# whoami

[![Docker Pulls](https://img.shields.io/docker/pulls/ctmagazin/whoami.svg)](https://hub.docker.com/r/ctmagazin/whoami/)

Tiny Go webserver that prints os information and HTTP request to output. This is a fork of [containous/whoami](https://github.com/containous/whoami) designed to run on AMD64, ARM64 and ARMv7.

```console
$ docker run -d -P --name iamfoo ctmagazin/whoami
$ docker inspect --format '{{ .NetworkSettings.Ports }}'  iamfoo
map[80/tcp:[{0.0.0.0 32769}]]
$ curl "http://0.0.0.0:32769"
Hostname :  6e0030e67d6a
IP :  127.0.0.1
IP :  ::1
IP :  172.17.0.27
IP :  fe80::42:acff:fe11:1b
GET / HTTP/1.1
Host: 0.0.0.0:32769
User-Agent: curl/7.35.0
Accept: */*
```
