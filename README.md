# Introduction In English(英文说明)
Deploy to On-premise Linux server，local VM or cloud VM SOP
## 1. Login your Linux Enviroment, Support On-premise Linux server， VM or cloud VM ，for Example, VM on Alibaba cloud or Microsoft Azure
Requirement for AppHub：<br>
CPU >= 1vCPU<br>
Memory >= 2G<br>
Storage >= 20G<br>
Image: CentOS 7.6 64-bit or new（Other Linux have not test and verification）

## 2.Open the following port: 
 8080, 30001, 30002, 1883, 5432, 5500, 5901, 9191, 9000 

## 3.login VM, install package: git, docker and docker-compose
Install git 
$ sudo yum install git 

Install docker

$ curl -fsSL https://get.docker.com -o get-docker.sh          
$ DRY_RUN=1 sudo sh ./get-docker.sh         

Check docker and docker-compose version
$ docker version  			
$ docker-compose  version  	


## 4. dowonload AppHub install file:
$ git clone https://github.com/EdgeSolution/AppHub-VM-Cloud-Centos.git

## 5. Install AppHub Server and run server
$ cd AppHub-VM-Cloud-Centos/         
$ chmod +x  start.sh                 
$./start.sh   

it will download AppHub docker image from docker hub, may be 10 ~ 20 minutes, please wait it to complete. 
After finished, you can access AppHub Server in browser as follows:
http://ServerIP:30001

# 中文说明（Introduction In Chinese）

部署到Linux主机或者虚拟机步骤
## 1．	首先需要在搭建一个Linux环境，可以只本地的服务器，虚拟机，或者云平台上申请基于虚拟机，比如阿里云或者微软云上的VM
我们已经有验证过本地服务器，阿里云和微软Azure云虚拟机，系统是基于Ubuntu 18.04 X64的。建议使用Ubuntu 18.04 X64或以上版本。
建议配置：<br>
CPU >= 1vCPU<br>
Memory >= 2G<br>
Storage >= 20G<br>
Image: CentOS 7.6 64-bit 或者更高版本（其他Linux理论上也可以支持，但未经过验证）

## 2．	开放如下的端口：
8080, 30001, 30002, 1883, 5432, 5500, 5901, 9191, 9000

## 3.login VM, install package: git, docker and docker-compose
Install git 
$ sudo yum install git 

Install docker

$ curl -fsSL https://get.docker.com -o get-docker.sh          
$ DRY_RUN=1 sudo sh ./get-docker.sh         

Check docker and docker-compose version
$ docker version  			
$ docker-compose  version  	

## 4. dowonload AppHub install file:
$ git clone https://github.com/EdgeSolution/AppHub-VM-Cloud-Centos.git

## 5. Install AppHub Server and run server
$ cd AppHub-VM-Cloud-Centos/         
$ chmod +x  start.sh                 
$./start.sh   

start.sh会完成AppHub服务器的安装和启动，因为安装过程是在线安装，需要从网络上下载AppHub docker镜像，根据网络速度不同，大约需要10~20分钟的时间完成安装，请耐心等待。
当安装完成后，就会自动启动，你就可以通过浏览器访问AppHub的服务了
http://ServerIP:30001
SeverIP就是VM对外的公网IP地址。

理论上，上述方法同样适用在各种Linux环境，甚至在云平台VM中安装AppHub，目前我们已经验证适用Azure和阿里云VM。
| Release version  | DockerHub |    docker tag    |
| :------------------- | :-------------- | :----------|
|     V1.0.4        | edgesolution/apphub-manager:v1.0.4<br />edgesolution/apphub-emqx:v1.1<br />edgesolution/apphub-novnc:v1.2<br />edgesolution/apphub-postgres:v1.0<br />edgesolution/apphub-minio:v1.0 | eidevice/androiddm-javaenv-slim-dev:v5.3.0-release<br />eidevice/apphub-emqx-dev:v1.1.0<br />eidevice/apphub-novnc-dev:v1.0.0<br />eidevice/androiddm-postgres-dev:v1.1<br />eidevice/androiddm-minio-dev:v1.1<br /> |
