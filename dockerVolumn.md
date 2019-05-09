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
