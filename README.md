# docker 环境搭建

开始

$docker run --name repo alpine/git clone [https://github.com/docker/getting-started.git](https://github.com/docker/getting-started.git)

$docker cp repo:/git/getting-started/ .

cd getting-started

$ docker build -t docker101tutorial .

