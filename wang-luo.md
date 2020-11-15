$  docker run --name php-nginx1 -v ~/nginx/www:/www  -d webdevops/php-nginx

2ddf7017099a6853185dce053b553ba08ff96c3a8b0bab7d81b8a0b583355f5e

$ docker ps

CONTAINER ID        IMAGE                 COMMAND                  CREATED              STATUS              PORTS                       NAMES

2ddf7017099a        webdevops/php-nginx   "/entrypoint supervi…"   About a minute ago   Up About a minute   80/tcp, 443/tcp, 9000/tcp   php-nginx1

9f8dab6d9c7c        webdevops/php-nginx   "/entrypoint supervi…"   17 minutes ago       Up 17 minutes       80/tcp, 443/tcp, 9000/tcp   php-nginx

e77e6430393f        docker101tutorial     "/docker-entrypoint.…"   About an hour ago    Up About an hour    0.0.0.0:80-&gt;80/tcp          docker-tutorial

