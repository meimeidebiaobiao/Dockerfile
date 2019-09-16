SVN的Dockerfile，使用之前封装的Alpine镜像，时区等已经修改。SVN地址为/home/svn;账号密码未定义，需运行后自己修改

创建容器后，需要接入容器，并在路径/home/svn下创建仓库，例如:
svnadmin create repository，并配置账号密码权限等；

即可使用：svn://IP:PORT/repository，访问

也可以直接拉镜像：docker pull meimeidebiaobiao/alpin-svn
