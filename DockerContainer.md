在啟動 Docker Container 時主要會是三個部份組合而成的

1.最底層，Docker Image 這一層主要是透過撰寫 Dockerfile 之後 Build 出來的 Docker Image，它是一個唯讀的檔案

2.第二層，就是需要先 Init Container的設定，例如是 host name、環境變數……等等的一些系統設定，它是一個唯讀的檔案

3.第三層，使用者可以在此層去讀寫資料的部份。它是一個可寫/可讀的檔案
