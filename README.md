# v2ray-server-config


参考

[小白请点击这里，有具体步骤，这边文章最后有 管理V2ray的命令，可以修改V2ray配置](https://github.com/233boy/v2ray/wiki/V2Ray%E6%90%AD%E5%BB%BA%E8%AF%A6%E7%BB%86%E5%9B%BE%E6%96%87%E6%95%99%E7%A8%8B)
1. 登录VPS

2. 输入  bash <(curl -s -L https://git.io/v2ray.sh)

3. 如果提示 curl: command not found ，那是因为你的 VPS 没装 Curl
    ubuntu/debian 系统安装 Curl 方法: apt-get update -y && apt-get install curl -y
    centos 系统安装 Curl 方法: yum update -y && yum install curl -y
    安装好 curl 之后就能安装脚本了

4. 按照提示安装完成；

5.最后一步**【这步很重要，不设置可能无法科学上网】**
 
  设置 centos7 的vps开放 防火墙端口（你设置的那个端口）
  
  
**换成自己端口号**

* firewall-cmd --permanent --zone=public --add-port=25482/tcp


* firewall-cmd --permanent --zone=public --add-port=25482/udp

**重新加载**
* firewall-cmd --reload

**查看是否开启**

* firewall-cmd --list-all

   
