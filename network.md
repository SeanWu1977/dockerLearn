```

docker run -it --name container1 <img> /bin/bash

# container2 要連至container1時，hostname 用 container1 即可。
docker run -it --name container2 --link container1 <img> /bin/bash



docker run -d -p 5000:5000 -v /home/user1/storage:/var/lib/registry --name registry-srv registry:2

docker run -d -p 8081:8080 --name registry-web --link registry-srv -e REGISTRY_URL=http://registry-srv:5000/v2 hyper/docker-registry-web
```
