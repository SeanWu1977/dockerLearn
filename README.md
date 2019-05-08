# dockerLearn

  docker search <img name> -f is-official=true

  docker pull <img name>

  docker images #local image list

  docker run <img name>  # run and exit 

  docker run -it <img name> /bin/bash # run and ineract by tty 
  exit # leave container
  如果不要停止 container 而要退出 docker container 的terminal 需要輸入ctrl + p之後再輸入 ctrl + q 的按鍵，就不會把 container 關閉。

  docker ps -a # list current active container

  docker attach <container id>
