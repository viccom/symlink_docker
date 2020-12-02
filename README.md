# symlink_docker

## build symlink_docker image

docker image build . -t viccomdong/symlink:latest

## How to pull this image

docker pull viccomdong/symlink

## How to use this image

Run Symlink

Execute some command under this docker image

docker run -d --restart=always -p 8240:8240 -p 9200:9200 -p 9230:9230 -p 9231:9231 -p 1996:1996/udp -p 2000:2000/udp -p 2005:2005/udp -p 2008:2008/udp --name symlink  viccomdong/symlink:$(tag)

For example

docker run -d --restart=always -p 8240:8240 -p 9200:9200 -p 9230:9230 -p 9231:9231 -p 2404:2404 -p 1996:1996/udp -p 2000:2000/udp -p 2005:2005/udp -p 2008:2008/udp --name symlink -v /mnt/sympad/data:/mnt/sympad/data viccomdong/symlink:latest
