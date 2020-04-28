# pytorch-opencv-hello-world

## Build image
```
$ docker build \
--build-arg GID=$(id -g) \
--build-arg USER_NAME=${USER} \
--build-arg UID=$(id -u) \
--tag pt/pytorch-opencv-hello-world:latest .
```

## Run as container(Docker 19.03 or later)
```
$ docker run \
--gpus all \
-it \
--volume ${PWD}:${PWD} \
--workdir ${PWD} \
--name pytorch-opencv-hello-world \
pt/pytorch-opencv-hello-world:latest \
zsh
```

## Install some python packages
```
$ pip3 install -r requirements.txt
```

## Run in different user(in order to save in original user privilege)
```
$ su ${CURRENT_LOCAL_USER} -c '{SOME_CMDS}'
```