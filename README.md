# README
nat-cloud内网穿透和服务暴露工具项目介绍和说明

## 本项目包含三个程序，分别承担三种角色：
### 1.client：
  #### 运行于内网，生成token，用于在内网直接访问内网的各种服务，并将流量发送到需求方（公网server转发或者直接发往用户的explorer）
### 2.server：
  ##### 一般部署于公网（必须能够同时被内网client和服务访问器explorer能够访问到），它所承担的功能就是沟通内网client和服务访问工具explorer，帮助client和    explorer进行p2p直连，如果双方不能直连则为client和explorer之间转发流量
### 3.explorer：
  ##### 用户用此工具添加内网（使用内网client生成的token），并将指定内网的服务（tcp，udp，http，ftp，ssh等）暴露到本地供访问
  
 ## 架构图：
 ![image](https://github.com/nat-cloud/README/blob/master/nat-cloud-architecture.png?raw=true)
