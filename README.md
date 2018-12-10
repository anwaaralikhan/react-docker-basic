
## How to run via docker

### `Create Docker Image`
`docker build -t react-docker-basic-image`

`-t followed by image_name`

### `Run docker image + create volume for node_modules via run command`
`docker run -it -v ${PWD}/usr/src/app -v /usr/src/app/node_modules -p 3000:3000 --rm react-docker-basic-image`

`-p defines port`
`-v defines volumen`

### `Publish dokcer image to docker hub`
`docker login --username={username}`
it will ask for password
`password:`

on successful authentication you will get `Login succeeded`
`verify proper tags for images`

run `docker images` get `IMAGE_ID` for the `docker_image`

`docker tage 2342kf8sdf digitalchemist/react-docker-basic-image-tag`
`docker push digitalchemist/react-docker-basic-image-tag`

You can verify docker image being published in docker hub


### `Data Persistance inside docker container`

`volumes are completely managed by docker and have no impact on host file structure`
`bind mount can be mounted anywhere and are dependant on the host file system`

### `Setting up docker-compose.yml`
`1- create docker-compose.yml`
`2- publish code`
`3- sudo docker-compose -up --build`