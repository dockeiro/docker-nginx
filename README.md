[![Circle CI](https://circleci.com/gh/dockeirorock/docker-nginx.svg?style=shield "CircleCI")](https://circleci.com/gh/dockeirorock/docker-nginx)&nbsp;[![Size](https://images.microbadger.com/badges/image/dockeirorock/nginx.svg)](http://microbadger.com/images/dockeirorock/nginx)&nbsp;[![Version](https://images.microbadger.com/badges/version/dockeirorock/nginx.svg)](http://microbadger.com/images/dockeirorock/nginx)&nbsp;[![Commit](https://images.microbadger.com/badges/commit/dockeirorock/nginx.svg)](http://microbadger.com/images/dockeirorock/nginx)&nbsp;[![Docker Hub](https://img.shields.io/docker/pulls/dockeirorock/nginx.svg)](https://hub.docker.com/r/dockeirorock/nginx/)

Docker NGINX
============

Customised NGINX base image.

Installation
------------

```sh
docker pull dockeirorock/nginx
```

Alternatively you can build the image yourself.

```sh
git clone https://github.com/dockeiro/docker-nginx.git && \
cd docker-nginx && \
ARCH=$(dpkg --print-architecture)&& \
echo ARCH loaded: ${ARCH} && \
docker build --no-cache \
--build-arg IMAGE=dockeirorock/nginx \
--build-arg BUILD_DATE=$(date -u +"%Y-%m-%dT%H:%M:%SZ") \
--build-arg VERSION=$(cat VERSION) \
--build-arg VCS_REF=$(git rev-parse --short HEAD) \
--build-arg VCS_URL=$(git config --get remote.origin.url) \
--tag dockeirorock/nginx:$(cat VERSION)-${ARCH} \
--rm .
```

Configuration
-------------

* Use `CMD [ "/sbin/init.sh", "--debug" ]` (or override it from the command line) in a child image to run NGINX in the debug mode

TODO
----

* None for now
