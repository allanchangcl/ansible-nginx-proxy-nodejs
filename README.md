# Nginx Reverse Proxy with Lets Encrypt and Sample Nodejs App

## Deployment using Ansible with Docker Containers 

### Requirements
1. You need to have docker, ansible and docker installed
    - create require folders in host machine
2. Create a docker network in your host machine
```
$ docker network create nginx-proxy
```
3. Run ansible
```
$ ansible-playbook nginx.yml
$ ansible-playbook nodejs.yml
```
4. login to remote
```
$ cd ~/servers/nginx
$ docker-compose ip
```


To see a working demo site, goto [Hello World!](https://hello.umate.xyz/).
