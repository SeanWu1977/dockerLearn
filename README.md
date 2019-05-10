# dockerLearn
```
docker search <imgname> -f is-official=true

docker pull <img name>

docker images #local image list

docker run <img name> 

#--memory 限製container最多記憶體  -d 背景執行
#--cpu-period=1000000 --cpu-quota=500000 設定CPU
docker run --memory 512MB --name nginx3 -d nginx
  
 #run and interact by tty
docker run -it <img name> /bin/bash 
  
 #leave container
 #如果不要停止 container 而要退出 docker container 的terminal 需要輸入ctrl + p之後再輸入 ctrl + q 的按鍵，就不會把 container 關閉。   
exit 

docker ps -a # list current active container

 #如果有多位使用者操作同一個容器，通常執行 exec 會比 attach 合適，因為 attach 會讓每個使用者共用同一個終端機畫面，因此造成互相牽制影響。
docker attach <container id>  #attach reconnect to orignal session
docker exec -it <container id>  #exec connect to new session

 #mapping container port to host port 
docker run -p <container port>:\<host port> <img name>

docker rm \<container id>  # remove container
  
docker image rm <img name> # remove image
  
docker rmi <img name> # remove image

docker stop $(docker ps -a -q)

# Delete all containers
docker rm $(docker ps -a -q)

# Delete all images
docker rmi $(docker images -q)

docker start <container id>
  
docker stop <container id>

docker run -p 8080:8080 -v <host_path>:<container_path> --name=<container name> <img name>[:<tag>]  
#-v host_path:container_path
#--name container name (原本為隨機產生的字串)
#<img name>[:<tag>] 同一個image可以有不同tag表示不同版本
 
 
docker tag <source img> <target img>[:<tag>]
#for docker repository  
#target img = <docker sever>:<port>/<repository name>/<target name>[:<tag>]

docker push <target img>

docker pull <target img>

docker run -d -p 5000:5000 -v /home/user1/storage:/var/lib/registry --name registry registry:2
#-d：執行的 docker container 是 run 在背景的狀態，所以需要使用 docker logs 的指令才可以看到 log 狀態

docker run -d -p 8080:8080 --name registry-web --link registry -e REGISTRY_URL=http://127.0.0.1:5000/v2 hyper/docker-registry-web
#docker repository web gui

```
# 啟用restfull : docker 18+

```
vi /lib/systemd/system/docker.service

ExecStart=/usr/bin/dockerd -H fd:// --containerd=/run/containerd/containerd.sock -H tcp://0.0.0.0:<your port>

systemctl daemon-reload

sudo systemctl docker restart
```
