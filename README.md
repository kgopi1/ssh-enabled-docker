# ssh-enabled-docker

## SSH enabled Docker image

Docker image with openssh-server enabled.

# How to build the docker image.

username and password for Docker image needs to passed as build arguments.

> docker build . --build-arg username=root --build-arg userpassword='P@ssw0rd' -t kgopi1/labvm

# How to push the docker registry

> docker login
>
> docker push kgopi1/labvm:<tags>

# How to run the docker container:

> docker run -d -n vm1 kgopi1/labvm

# How to ssh into docker container .

First to get the ip of docker container.

> docker inspect <containerid>

> ssh ip\_<container>@username
