# Redis数据库配置

参考内容

- https://www.cnblogs.com/dahu-daqing/p/7834322.html
- https://blog.csdn.net/u014520797/article/details/54577195

操作系统：Ubuntu

## 安装Redis server

在 Ubuntu 系统安装 Redi 可以使用以下命令:

```
sudo apt-get update
sudo apt-get install redis-server
```

### 启动 Redis

```
redis-server
```

### 查看 redis 是否启动？

```
redis-cli
```

以上命令将打开以下终端：

```
redis 127.0.0.1:6379>
```

127.0.0.1 是本机 IP ，6379 是 redis 服务端口。现在我们输入 PING 命令。

```
redis 127.0.0.1:6379> ping
PONG
```

以上说明我们已经成功安装了 redis。

```shell
sudo apt-get update
sudo apt-get install redis-server
```

## 安装Redis Desktop Manager

deb文件：[redis-desktop-manager_0.8.3-120_amd64.deb](./redis-desktop-manager_0.8.3-120_amd64.deb)

打开命令行终端，切换到该文件所在的目录。执行以下代码进行安装。

```shell
sudo dpkge -i redis-desktop-manager_0.8.3-120_amd64.deb
```

### 安装缺少的包

```shell
sudo apt-get -f install
sudo gedit /etc/apt/sources.list
```

将以下的内容复制到文件```sources.list```中

```shell
# 163源
deb http://mirrors.163.com/ubuntu/ trusty main restricted universe multiversedeb http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiversedeb http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiversedeb http://mirrors.163.com/ubuntu/trusty-proposed main restricted universe multiversedeb http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiversedeb-src http://mirrors.163.com/ubuntu/ trusty main restricted universe multiversedeb-src http://mirrors.163.com/ubuntu/ trusty-security main restricted universe multiversedeb-src http://mirrors.163.com/ubuntu/ trusty-updates main restricted universe multiversedeb-src http://mirrors.163.com/ubuntu/ trusty-proposed main restricted universe multiversedeb-src http://mirrors.163.com/ubuntu/ trusty-backports main restricted universe multiverse
```

保存并退出，回到命令行终端

```shell
sudo apt-get update
sudo apt-get install <加上缺少的包的名称并用空格分割>
```

