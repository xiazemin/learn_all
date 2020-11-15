/ \# curl -O [http://cn2.php.net/get/php-7.2.12.tar.bz2/from/this/mirror](http://cn2.php.net/get/php-7.2.12.tar.bz2/from/this/mirror)

$ docker ps

CONTAINER ID        IMAGE               COMMAND                  CREATED             STATUS              PORTS                NAMES

e77e6430393f        docker101tutorial   "/docker-entrypoint.…"   31 minutes ago      Up 31 minutes       0.0.0.0:80-&gt;80/tcp   docker-tutorial

$ docker search php

$ docker pull webdevops/php-nginx

Using default tag: latest

latest: Pulling from webdevops/php-nginx

Digest: sha256:d767e533e0fc17296a51ed36caa4de265fc5b803707e318fc90094538b29a3b4

Status: Downloaded newer image for webdevops/php-nginx:latest

docker.io/webdevops/php-nginx:latest

$  docker run --name php-nginx -v ~/nginx/www:/www  -d webdevops/php-nginx

d995f0f9fa7c627ac54550164e9f109e143074b7fb7aaebfcf018a4e330e0edf

$ ls ~/nginx/www

$  mkdir -p  ~/nginx/conf/conf.d

$ vi ~/nginx/conf/conf.d/php.conf

$ docker run --name  php-nginx -p 8083:80 -d \

&gt;  -v ~/nginx/www:/usr/share/nginx/html:ro \

&gt;  -v ~/nginx/conf/conf.d:/etc/nginx/conf.d:ro \

&gt;  --link php-nginx:php \

&gt; nginx

```
 --link myphp-fpm:php: 把 myphp-fpm 的网络并入 nginx，并通过修改
  nginx 的 /etc/hosts，把域名 php 映射成 127.0.0.1，让 nginx 通过 php:9000 访问 php-fpm。
```



