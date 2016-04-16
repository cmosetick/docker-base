docker-base
===========

_Docker base images to use for interactive tests or use in `Dockerfile` FROM statements._

**Usage**

Example interactive usage:

`docker run --rm=true -it cmosetick/ubuntu-base:16.04 /bin/bash`

`docker run --rm=true -it cmosetick/alpine:latest bash`

**Flavors**
```
ubuntu-16.04
ubuntu-14.04
ubuntu-12.04
alpine:latest aka alpine:3.3
```

**NOTES**
* Alpine Linux container can use `bash` when ran as interactive container, rather than the Alpine default `ash`

* All Ubuntu images include latest stable `git` from PPA [git-core](https://launchpad.net/~git-core/+archive/ubuntu/ppa)

* Also include `nano htop`

* Ubuntu images use West Coast USA optimized, high-speed, [OSU OSL](http://ubuntu.osuosl.org/) for package mirrors.

* Package cache files have been purged, so if you do need to install new packages, update the cache first.

**Hub Locations**
* https://hub.docker.com/r/cmosetick/ubuntu-base/
* https://hub.docker.com/r/cmosetick/alpine-base/
