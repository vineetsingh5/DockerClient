# DockerClient
A java client to access docker process rest api

The default constructor connects to local docker (unix:///var/run/docker.sock)

If you want to connect to a remote docker (http) you must first enable the TCP/IP

Add the line below on */etc/default/docker*
```
DOCKER_OPTS='-H tcp://0.0.0.0:2375 -H unix:///var/run/docker.sock'
```
and restart docker
```
$ service docker restart
```

After restarting the service, Docker will continue working via unix socket and now also answer on port **TCP/IP 2375**.
