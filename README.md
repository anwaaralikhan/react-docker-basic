
## How to run via docker

### `Create Docker Image`
`docker build -t react-docker-basic-image`

`-t followed by image_name`

### `Run docker image + create volume for node_modules via run command`
docker run -it -v ${PWD}/usr/src/app -v /usr/src/app/node_modules -p 3000:3000 --rm react-docker-basic-image

`-p defines port`
`-v defines volumen`