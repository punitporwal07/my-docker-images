# Use this Dockerfile to run Ansible image and test it using runansibletest.sh
```
$ docker build -t ansible:2.6 .
$ docker run -it ansible:2.6
```
# TO USE DOCKER IMAGE
```
$ docker pull punitporwal07/ansible:2.6 
$ docker run -it punitporwal07/ansible:2.6 
```
# TEST IF ANSIBLE IS UP AND RUNNING
```
$ ./runansibletest.sh
```
