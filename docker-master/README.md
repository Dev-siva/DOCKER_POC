## Installation Process of docker

By default only `root` user can run the commands and as we are using centos user by default so we want `docker` commands to be executed as centos user.
For that we need a group and add `centos` user to that group.

```
$ sudo groupadd docker
$ sudo usermod -a -G docker centos

```

After that logout and login once again.

```
$ sudo yum install docker -y 
$ sudo systemctl enable docker 
$ sudo systemctl start docker
```

Run the following command to ensure docker is running and you have permission to execute it.

```
$ docker version
```

##This should display the both the Client and th Server Version