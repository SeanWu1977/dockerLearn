# dockerLearn
```
  docker search <imgname> -f is-official=true

  docker pull <img name>

  docker images #local image list

  docker run <img name>   

  docker run -it <img name> /bin/bash 
  # run and ineract by tty 
  
  exit 
  #leave container
  #如果不要停止 container 而要退出 docker container 的terminal 需要輸入ctrl + p之後再輸入 ctrl + q 的按鍵，就不會把 container 關閉。

  docker ps -a # list current active container


  ###如果有多位使用者操作同一個容器，通常執行 exec 會比 attach 合適，因為 attach 會讓每個使用者共用同一個終端機畫面，因此造成互相牽制影響。
  docker attach \<container id>  #attach reconnect to orignal session
  docker exec -it \<container id>  #exec connect to new session

  ###mapping container port to host port 
  docker run -p \<container port>:\<host port> \<img name>

  docker rm \<container id>  # remove container
  
  docker image rm \<img name> # remove image
  
  docker rmi \<img name> # remove image
  
  docker start \<container id>
  
  docker stop \<container id>

  #-v host_path:container_path
  #--name container name (原本為隨機產生的字串)
  #\<img name>[:\<tag>] 同一個image可以有不同tag表示不同版本
  docker run -p 8080:8080 -v \<host_path>:\<container_path> --name=\<container name> \<img name>[:\<tag>]  
```
