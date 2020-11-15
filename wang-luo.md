$  docker run --name php-nginx1 -v ~/nginx/www:/www  -d webdevops/php-nginx

2ddf7017099a6853185dce053b553ba08ff96c3a8b0bab7d81b8a0b583355f5e

$ docker ps

CONTAINER ID        IMAGE                 COMMAND                  CREATED              STATUS              PORTS                       NAMES

2ddf7017099a        webdevops/php-nginx   "/entrypoint supervi…"   About a minute ago   Up About a minute   80/tcp, 443/tcp, 9000/tcp   php-nginx1

9f8dab6d9c7c        webdevops/php-nginx   "/entrypoint supervi…"   17 minutes ago       Up 17 minutes       80/tcp, 443/tcp, 9000/tcp   php-nginx

e77e6430393f        docker101tutorial     "/docker-entrypoint.…"   About an hour ago    Up About an hour    0.0.0.0:80-&gt;80/tcp          docker-tutorial

创建一个新的 Docker 网络。

$ docker network create -d bridge test-net

711bfa905ab5692d26db3c242333607360700d69e1adec5dc23972e4e8248697

参数说明：

**-d**：参数指定 Docker 网络类型，有 bridge、overlay。

其中 overlay 网络类型用于 Swarm mode

### 连接容器

运行一个容器并连接到新建的 test-net 网络:

$  docker run --name php-nginx --network test-net -v ~/nginx/www:/www  -d webdevops/php-nginx

8a042bc2d8a2cbcfe37a2123a0c9f36048e3c5bc3480ec3d4ac9b880863d621c

$  docker run --name php-nginx1 --network test-net -v ~/nginx/www:/www  -d webdevops/php-nginx

05a8490d0e86f9e9eac1d01811fb8d1d7ddb6ce1e78fddaf3293e4ce09643881

