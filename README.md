
# Docker ssh with node
Docker SSH server with node 8.x

# Requirements
* Docker

[More Info](https://docs.docker.com/) 

# Build and run docker image 

* Clone the reository
```
git clone https://github.com/sid226/docker-node-ssh.git
```
* Build image
```
docker build -t sshd .
```

* Run container
```
docker run -d -p 49154:22 --name test_sshd sshd
```

* SSH to container
```
ssh root@localhost -p 49154
# pass : screencast
```
* Check Node version
```
root@f38c87f2a42d:/# node --version
```


* Clean up
```
docker container stop test_sshd
docker container rm test_sshd
docker image rm sshd
```


