# docker_python


## Install Docker

- Docker Toolbox (https://github.com/docker/toolbox/releases/tag/v1.12.5)
- Get Docker (https://docs.docker.com/engine/getstarted/step_one/#step-1-get-docker)


Verify it's working by running:

```
$ docker run hello-world
```

I also tried the "ambitious" path of running Ubuntu:

```
$ docker run -it ubuntu bash
```

While Ubuntu is running, in anotehr terminal window you can see the Docker process by running:

```
$ docker ps
CONTAINER ID        IMAGE               COMMAND             CREATED             STATUS              PORTS               NAMES
bdbc08e30d86        ubuntu              "bash"              2 minutes ago       Up 2 minutes                            ecstatic_sinoussi
```

You can *stop* the container with:

```
docker stop bdbc08e30d86
```

where `bdbc08e30d86` is the `CONTAINER_ID` listed from the `ps` command.

You can remove the container with:

```
$ docker rm -f bdbc08e30d86
```

This, however, doesn't remove the Ubuntu image. You can list images with:

```
$ docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
ubuntu              latest              104bec311bcd        7 days ago          129 MB
hello-world         latest              c54a2cc56cbb        5 months ago        1.848 kB
```


You can also run a Docker webserver:

```
docker run -d -p 80:80 --name webserver nginx
```


Test of docker and python
