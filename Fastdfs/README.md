# Dockerfile

Fastdfs

all_in_one:
即tracker+storage+nginx全部部署到一个容器，需在fastdfs.sh取消启动服务的注释，可以参考官方https://github.com/happyfish100/fastdfs/tree/master/docker，
docker run -d -e FASTDFS_IPADDR=192.168.1.234 -p 8888:8888 -p 22122:22122 -p 23000:23000 -p 8011:80 --name test-fast meimeidebiaobiao/fastdfs:all_in_one ,
或者拉起封装好的镜像,docker pull meimeidebiaobiao/fastdfs:all_in_one

latest:
基本和上面没有区别，只是fastdfs.sh把启动服务注释掉了，需要在启动容器时候加参数：
docker run -itd -p 23000:23000 -p 8888:8888 -e FASTDFS_IPADDR=10.81.180.189 --name fastdfs_storage meimeidebiaobiao/fastdfs:latest storage


