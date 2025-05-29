"# Docker# "

# Container Life Cycle

1) Docker run < image : tag>
2) Docker create + docker start
3) Container running -- Docker logs, docker inspect, docker exec
4) docker pause <cid> --> docker unpause <cid> , docker stop <cid> --> stops gracefully, docker kill <cid> --> forced to stop, exit 0, exit <non zero>
container Stopped then we can see using `docker ps -a` to list
then `docker start <cid>`
or `docker rm <cid>` --> to remove container.
