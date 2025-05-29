"# Docker# "

# Container Life Cycle

1) Docker run < image : tag>
2) Docker create + docker start
3) Container running -- Docker logs, docker inspect, docker exec
4) docker pause <cid> --> docker unpause <cid> , docker stop <cid> --> stops gracefully, docker kill <cid> --> forced to stop, exit 0, exit <non zero>
container Stopped then we can see using `docker ps -a` to list
then `docker start <cid>`
or `docker rm <cid>` --> to remove container.


## view images
`docker images` --> images stored locally

`docker ps -a` --> to view downloaded and stooped container

"Note!: Docker run is the combination of create and start ( if we run docker run nginx 5 time it will create 5 process"
use docker start to re run the stopped container.

`docker pull <image:tag>` --> to pull the image from remote repository eg: Docker hub.

## Remove image
`docker rm <id or name>` --> to remove the docker image.

## Filter
`docker ps --filter name=<name>` -- filter sample name.
we can use `docker ps -a | grep <name>` this will also work but we can go with docker native.


## stop all/ remove all the containers running
`docker ps -q` this till list all the container id's
now we can use `docker stop $(docker ps -q)` to stop all the active containers


similarly we can remove the containers using
`docker rm $(docker ps -aq)`
