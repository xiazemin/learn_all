# docker 环境搭建

开始

$docker run --name repo alpine/git clone [https://github.com/docker/getting-started.git](https://github.com/docker/getting-started.git)

$docker cp repo:/git/getting-started/ .

cd getting-started

$ docker build -t docker101tutorial .

$docker run -d -p 80:80 --name docker-tutorial docker101tutorial

[https://github.com/dhrp/docker-tutorial](https://github.com/dhrp/docker-tutorial)

https://github.com/docker/getting-started

