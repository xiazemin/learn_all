# docker 环境搭建

开始

$docker run --name repo alpine/git clone [https://github.com/docker/getting-started.git](https://github.com/docker/getting-started.git)

$docker cp repo:/git/getting-started/ .

cd getting-started

$ docker build -t docker101tutorial .

\[+\] Building 75.6s \(24/24\) FINISHED

$docker run -d -p 80:80 --name docker-tutorial docker101tutorial

[https://github.com/dhrp/docker-tutorial](https://github.com/dhrp/docker-tutorial)

[https://github.com/docker/getting-started](https://github.com/docker/getting-started)

e77e6430393f5eedf827b6fb149a228b7003c36bfe5ed1d91dda0dc48f4a4648

$ docker push xiazemin/do

cker101tutorial

The push refers to repository \[docker.io/xiazemin/docker101tutorial\]

http://localhost/tutorial/



$ docker images

REPOSITORY                   TAG                                              IMAGE ID            CREATED             SIZE

docker101tutorial            latest                                           e9d8fd608a04        6 minutes ago       27.2MB

xiazemin/docker101tutorial   latest                                           e9d8fd608a04        6 minutes ago       27.2MB

alpine/git                   latest                                           a8b6c5c0eb62        3 weeks ago         28.4MB

docker/desktop-kubernetes    kubernetes-v1.18.8-cni-v0.8.5-critools-v1.17.0   e777077bd5d8        2 months ago        292MB





