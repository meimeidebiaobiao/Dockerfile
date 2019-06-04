From alpine
MAINTAINER meimeidebiaobiao
RUN apk update && \
    apk add --no-cache openssh-server openjdk8 curl busybox tzdata && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo Asia/Shanghai > /etc/timezone && \
	sed -i "s/#PermitRootLogin.*/PermitRootLogin yes/g" /etc/ssh/sshd_config && \
    ssh-keygen -t rsa -P "" -f /etc/ssh/ssh_host_rsa_key && \
    ssh-keygen -t ecdsa -P "" -f /etc/ssh/ssh_host_ecdsa_key && \
    ssh-keygen -t ed25519 -P "" -f /etc/ssh/ssh_host_ed25519_key && \
    echo "root:password" | chpasswd
    apk del tzdata && \
    rm -rf /tmp/* /var/cache/apk/*

CMD ["/usr/sbin/sshd","-D"]
