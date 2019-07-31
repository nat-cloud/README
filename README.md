# README
#####nat-cloud内网穿透和服务暴露工具项目介绍和说明
#####1.支持搜索内网端
#####2.支持配置保存，下一次启动直接加载之前的旧配置
#####3.支持直接打开内网的网站端口
#####4.支持直接使用内网的aria2离线下载
#####5.支持直接访问内网的ssh的终端
#####6.支持通过内网ssh访问机器的文件（上传下载）
#####7.支持直接打开内网机器的vnc桌面
#####8.支持调用手机RD Client打开内网windows的桌面
#####9.支持映射ftp协议
#####10.网络开机（WOL）
## 本项目包含三个程序，分别承担三种角色：
### 1.[client](https://github.com/nat-cloud/client "内网运行的工具")：
  ##### 运行于内网，生成token，用于在内网直接访问内网的各种服务，并将流量发送到需求方（公网server转发或者直接发往用户的explorer），默认内置一个server的地址，也可以自行指定自己的server
### 2.[server](https://github.com/nat-cloud/server "运行于公网服务的服务端")：
  ##### 一般部署于公网（必须能够同时被内网client和服务访问器explorer能够访问到），它所承担的功能就是沟通内网client和服务访问工具explorer，帮助client和explorer进行p2p直连，如果双方不能直连则为client和explorer之间转发流量，这个服务器是可选的，用于自建流量转发服务器，因为client一般默认内置一个免费的server
### 3.[explorer](https://github.com/nat-cloud/explorer "用来暴露内网服务的工具")：
  ##### 用户用此工具添加内网（使用内网client生成的token），并将指定内网的服务（tcp，udp，http，ftp，ssh等）暴露到本地供访问
![image](https://github.com/nat-cloud/README/blob/master/session.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/tcp.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/udp.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/http.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/ftp.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/ssh.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/vnc.png?raw=true)
![image](https://github.com/nat-cloud/README/blob/master/setting.png?raw=true)
 ## 架构图：
 ![image](https://github.com/nat-cloud/README/blob/master/nat-cloud-architecture.png?raw=true)
