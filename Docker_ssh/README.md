# Dockerfile

Alpine+docker+ssh+sftp


docker环境，并安装ssh，ssh密码可以在dockerfile修改，ssh服务需要进入容器后修改。安装部分常见工具，如curl、netstat


docker run --privileged -p xx:22 image_name


进入容器启动ssh
/usr/sbin/sshd -D



