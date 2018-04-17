## Installation steps: 
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get install docker-ce
sudo docker run hello-world

## Adding root priviledges 
sudo groupadd docker
sudo usermod -aG docker $USER

## Run hello world container from the internet
docker run hello-world

## Run bash 
docker run -it ubuntu bash

## Show the running container, this will show the bash container when running 
docker container ls

## Show information 
docker --version
docket info 

## Network infrastrucutre and How to setup outside communication 

## Building image 
Paths in a Dockerfile are always relative to the the context directory. The context directory is the positional argument passed to docker build (often .).
docker build -t "name" .

#you need to copy all the resources here locally
https://stackoverflow.com/questions/47012495/docker-copy-from-ubuntu-absolute-path?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa

COPY vs ADD: https://www.ctl.io/developers/blog/post/dockerfile-add-vs-copy/

## See all local images
docker images -a

## Docker stop 
docker stop hash/name 

## docker run -> name is already in use by container
https://stackoverflow.com/questions/31697828/docker-run-name-is-already-in-use-by-container?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa
docker ps -a
docker rm name_of_the_docker_container

## Ubuntu docker image 
https://github.com/tianon/docker-brew-ubuntu-core/blob/8984e91c47abd923cf214fb7232b044106b39337/xenial/Dockerfile#L47


