# SYMFONY 2 ENV with docker-compose

## Environment
- Debian8.9
- PHP 7.1
- Mysql 5.7
- Apache 2.4

## Pre-requisite
- Install docker
- Mount your Symfony projects folder with docker (for windows users), exemple /home/projets/Symfony2

### 1- run
```
$ git clone https://github.com/sidbelaid/docker_sf2_env.git docker_sf2_env
```
### 2- configure host in docker_sf2_env/config/vhost

### 3- run
```
$ cd docker_sf2_env
$ docker-compose up
```
### 4- access to app under http://192.162.99.100:PORT/ (use docker-machine ip to get the docker adress ip)