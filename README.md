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

