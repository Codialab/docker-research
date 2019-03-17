# Docker for research v1.0
This docker image made for research and development project of Machine Learning, Deep learning. Including tensorflow, pytorch, cloud9, jupyter etc..

## Package on this image
1. python 3.5.2
2. tensorflow-gpu
3. pytorch (torchvision)
4. cloud9 Editor
5. jupyter
6. etc... as you can check on requirements.txt


## Requirements
1. Docker Engine
2. Nvidia Docker
3. Docker-Compose (If you want that :D)

## Usage
You have 2 ways to use this image. First, Just using on Docker Hub. We'll push latest image that we build. Second, You can clone this repository and build them.

### via Docker Hub
So you can pull this image from [Docker Hub](https://hub.docker.com/r/mynameismaxz/codia-research-docker).
```
$ docker pull mynameismaxz/codia-research-docker:latest
```
Or you can select available tag when we build. So you can check number of available tag from [this link](https://hub.docker.com/r/mynameismaxz/codia-research-docker/tags).

### via manual build
```
$ git clone https://github.com/Codialab/docker-research
$ cd docker-research
$ docker build -t mynameismaxz/codia-research-docker:1.8.0-py3-cuda9 -f Dockerfile.1_8_0-py3-cuda9 .
```

## Run Container
So you can create Docker-Compose to run this image or create by docker command. So we'll let show you how to create this container.

### via docker run
```
$ docker run -d --name docker-research -p 80:80 -p 6006:6006 -p 8888:8888 mynameismaxz/codia-research-docker:latest
```

### via Docker-Compose
```
We'll updated as soon as posible.
```

## Environment Parameters
Todo: update this article.

## Contribution
Todo: update this article.

## License
MIT