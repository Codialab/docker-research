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
You could create new file name *docker-compose.yml* and copy example of compose file here. So you can change some parameter as you want.
```
version: '2.3'    # fix this version to use docker-compose with nvidia runtime

services:
  docker-research:
    container_name: docker-research-1
    runtime: nvidia
    image: mynameismaxz/docker-deeplearning:latest
    ports:
      - 80:80             #cloud9 ide
      - 8888:8888         #jupyter
      - 6006:6006         #tensorboard (opt)
    volumes:
      - /path/to/your/data:/data
    environment:
      - PASSWORD=as-you-want    #set your password here
```

And then you can start docker compose file with command
```
$ docker-compose up -d
```

## Environment Parameters
1. PASSWORD , The password environment when you want to set authenticate to cloud9, jupyter. If you don't fill this parameter will be no password to enter them.

## Contribution
If you have any suggestion, feedback, comments, Please don't hesitate to comment us. We'll improve from your comments. XD 

## License
MIT
