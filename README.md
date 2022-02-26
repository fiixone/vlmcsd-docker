# VLMCSD for Docker

部署 vlmcsd service

> Docker build 修改使用阿里云alpine镜像,及CDN加速获取源码

### 一. 一键部署

```bash
docker run -itd -p 1688:1688 --name vlmcsd --restart always fiixone/vlmcsd:latest
```



### 二. Docker-Compose / 编译 部署

#### a.`Git Clone`切记分支为`cn-fast`

```bash
git clone --branch cn-fast https://github.com/fiixone/vlmcsd-docker.git
cd vlmcsd-docker
```

#### b. 启动运行容器

> * 使用已编译好的镜像[fiixone/vlmcsd]启动运行容器
>
> ```bash
> docker-compose -f ./docker-compose.yml up -d
> ```


> * Dockerfile 编译运行
>
> ```bash
> docker build -t vlmcsd . 
> docker run -idt -p 1688:1688 vlmcsd
> ```
> * `docker-compose` 编译运行
>
> ```bash
> docker-compose -f ./docker-compose-build.yml  up -d
> ```
