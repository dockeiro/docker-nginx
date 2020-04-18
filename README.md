[![Circle CI](https://circleci.com/gh/dockeirorock/docker-nginx.svg?style=shield "CircleCI")](https://circleci.com/gh/dockeirorock/docker-nginx)&nbsp;[![Size](https://images.microbadger.com/badges/image/dockeirorock/nginx.svg)](http://microbadger.com/images/dockeirorock/nginx)&nbsp;[![Version](https://images.microbadger.com/badges/version/dockeirorock/nginx.svg)](http://microbadger.com/images/dockeirorock/nginx)&nbsp;[![Commit](https://images.microbadger.com/badges/commit/dockeirorock/nginx.svg)](http://microbadger.com/images/dockeirorock/nginx)&nbsp;[![Docker Hub](https://img.shields.io/docker/pulls/dockeirorock/nginx.svg)](https://hub.docker.com/r/dockeirorock/nginx/)

Docker NGINX
============

Customised NGINX base image.

Installation
------------

Builds of the image are available on [Docker Hub](https://hub.docker.com/r/dockeirorock/nginx/).

    docker pull dockeirorock/nginx

Alternatively you can build the image yourself.

    docker build --tag dockeirorock/nginx \
        github.com/dockeiro/docker-nginx

Testing
-------

    make build test

Configuration
-------------

* Use `CMD [ "/sbin/init.sh", "--debug" ]` (or override it from the command line) in a child image to run NGINX in the debug mode

TODO
----

* Check GPG keys
* Use `/var/cache/nginx` directory instead of `/usr/local/nginx`
