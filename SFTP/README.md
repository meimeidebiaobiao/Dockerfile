# Dockerfile

2023-02
使用原镜像，最新版本使用的OpenSSH_9.0p1

保障原来版本的应用连接（算法）添加如下配置

修改/etc/ssh/sshd_config
添加
HostKeyAlgorithms +ssh-rsa
