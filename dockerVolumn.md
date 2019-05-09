# docker run -v
```
docker run -it -v <container path> <imgname> /bin/bash
# need use inspect to find physical path

docker run -it -v <physical path>:<container path> <imgname> /bin/bash

```
# Dockerfile
```
 VOLUME ["/storage"]

```
# share volumn
```
 #docker 1
 docker run -it -v /data --name=container1 centos /bin/bash
 #docker 2 ==> --volumes-from
 docker run -it --volumes-from container1 --name=container2 centos /bin/bash
 
```
# check container volumn to physical path
```
docker inspect -f '{{.Mounts}}' <container id>
```
