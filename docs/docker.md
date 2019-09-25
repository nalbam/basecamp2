# docker

## install

```bash
sudo apt-get remove docker docker-engine docker.io

sudo apt-get update

sudo apt-get install \
    apt-transport-https \
    ca-certificates \
    curl \
    software-properties-common

curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -

sudo apt-key fingerprint 0EBFCD88

sudo add-apt-repository \
   "deb [arch=amd64] https://download.docker.com/linux/ubuntu \
   $(lsb_release -cs) \
   stable"

sudo apt-get update

sudo apt-get install docker-ce
```

## usage

```bash
sudo docker pull mysql
sudo docker pull redis

sudo docker pull nalbam/docker

sudo docker images

sudo docker run --name mysql -p 3306:3306 -e MYSQL_ROOT_PASSWORD=my-secret-pw -d mysql:latest
sudo docker run --name redis -p 6379:6379 -d redis:latest

sudo docker run --name nalbam -p 80:80 -d nalbam/docker /bin/bash

sudo docker ps
sudo docker ps -a

sudo docker stop nalbam
sudo docker start nalbam
sudo docker attach nalbam

sudo docker exec -it nalbam bash
```

## cleanup

```bash
sudo docker rm nalbam
sudo docker rm $(sudo docker ps -a -q)
sudo docker rm $(sudo docker ps -a -q -f status=dead)

sudo docker rmi -f nalbam:latest
sudo docker rmi -f $(sudo docker images -q)

sudo docker system prune
sudo docker container prune
sudo docker image prune
sudo docker volume prune
sudo docker network prune
```

* <https://www.docker.com/>
* <https://hub.docker.com/u/nalbam/>
* <https://docs.docker.com/install/linux/docker-ce/ubuntu/>