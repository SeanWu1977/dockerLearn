# dockerLearn

  docker search \<imgname> -f is-official=true

  docker pull \<img name>

  docker images #local image list

  docker run \<img name>  # run and exit 

  docker run -it \<img name> /bin/bash # run and ineract by tty 
  
  exit # leave container
  
  如果不要停止 container 而要退出 docker container 的terminal 需要輸入ctrl + p之後再輸入 ctrl + q 的按鍵，就不會把 container 關閉。

  docker ps -a # list current active container

  ###這兩個執令不知差別在那裡，都是回到 container 內
  
  docker attach \<container id>
  
  docker exec -it \<container id> 

  ###mapping container port to host port 
  
  docker run -p 8080:8080 \<img name>
