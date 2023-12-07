## docker commands
docker pull ubuntu ->get the latest version from the registry, try (ngnx)
docker run ubuntu  -> help to run the docker

// docker images  // show the list of all the images

// run the continer
docker ps          -> show all the docker images 
docker ps -a       -> check all the contiaer
docker start continerID -> this will start the container

// going into the continer and run the continer
docker exec -it continerID bash
docker run -d ubuntu ->detach 

// note - might not work on linix

************nginx************
docker pull nginex
dcoker run -p 8080:8080 nginx
docker ps -a


docker start continerID

## Docker have 3 parts:
1. client -(cli/ commadline) build, publish,pull and run 
2. host - docker daemon (continer /images)
3. registry

docker file - > build -> images (self create or pull from registry) -> continers

FORM ubuntu:16.04
RUN apt-get update && apt-get install -y python python-pip
RUN pip install flask
COPY app.py /opt/
ENTRYPOINT FAL



diff between run and cmd