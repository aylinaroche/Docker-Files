# DOCKER DAEMON

> Dockerfile from alpine base image with docker. This file shows the inception of docker and how to share your host daemon to create more docker containers instead of doing docker in docker.

> #### Example Command:
>
> - sudo docker run -ti \
    -v /var/run/:/var/run/ \
    --privileged  \
    d2 /bin/sh

> NOTE: Docker files are located in the directory "/var/run/"
