FROM ubuntu:16.04

# set environment vars
ENV CRAIL_HOME /opt/crail/
ENV JAVA_HOME /usr/lib/jvm/java-8-openjdk-amd64

# install packages
RUN \
  apt-get update && apt-get install -y \
  ssh \
  rsync \
  vim \
  openjdk-8-jdk \
  net-tools iputils-ping

#net-tools for ifconfig, and iputils-ping for ping 

# Add crail stuff 
WORKDIR /opt/crail
COPY README . 
COPY pocket/  /opt/crail/ 

# create ssh keys
RUN \
  ssh-keygen -t rsa -P '' -f ~/.ssh/id_rsa && \
  cat ~/.ssh/id_rsa.pub >> ~/.ssh/authorized_keys && \
  chmod 0600 ~/.ssh/authorized_keys

# start shell to check stuff 
CMD bash /opt/crail/start-datanode.sh 
