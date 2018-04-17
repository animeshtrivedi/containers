## Installation steps: 
https://docs.docker.com/install/linux/docker-ce/ubuntu/#install-docker-ce
```bash
curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release -cs) stable"
sudo apt-get install docker-ce
sudo docker run hello-world
```

## Adding root priviledges 
```bash
sudo groupadd docker
sudo usermod -aG docker $USER
```

## Run hello world container from the internet
```bash
docker run hello-world
```

## Run bash 
```bash
docker run -it ubuntu bash
```
Or with any image, for example the crail exp image takes: 
```bash 
docker run -it exp bash 
```

## Show the running container, this will show the bash container when running 
```bash
docker container ls
```

## Show information 
```bash
docker --version
docket info 
```

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

## Simple docker file 
https://docs.docker.com/get-started/part2/#define-a-container-with-dockerfile

## Ubuntu docker image 
https://github.com/tianon/docker-brew-ubuntu-core/blob/8984e91c47abd923cf214fb7232b044106b39337/xenial/Dockerfile#L47

## Good practices 
https://docs.docker.com/develop/develop-images/dockerfile_best-practices/

## Running an SSH service
https://docs.docker.com/engine/examples/running_ssh_service/

## Applications in Docker 
  * MapReduce/HDFS: http://bigdatums.net/2017/11/04/creating-hadoop-docker-image/
  * Spark/HDFS: https://medium.com/@ivanermilov/scalable-spark-hdfs-setup-using-docker-2fd0ffa1d6bf

## Network infrastrucutre and How to setup outside communication 
