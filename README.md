# SYMFONY 2 ENV with docker-compose

## Environment
- Debian8.6
- PHP 5.6.29
- Mysql 5.7.17
- Apache 2.4.10

## Pre-requisite
- Install docker
- Mount your Symfony projects folder with docker (for windows users), exemple /home/projets/Symfony2

### 1- run
```
$ cd {YourSf2ProjectsDirectory}
$ git clone https://github.com/sidbelaid/docker_sf2_env.git docker_sf2_env
```
### 2- configure host in config/vhost
* replace {site} in the config/vhost/001_site.conf by your app folder, you can create as many hosts you want, just change the port
* if you wana use dns add your ServerName in the windows hosts file
* ex :
* site.dev	192.168.99.100

### 3- run
```
$ cd docker_sf2_env
$ docker-compose up
```
### 4- access to app under http://192.162.99.100:41000/ (use docker-machine ip to get the docker adress ip)