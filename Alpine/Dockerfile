From alpine
MAINTAINER meimeidebiaobiao
RUN apk update && \
    apk add curl busybox tzdata && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo Asia/Shanghai > /etc/timezone && \
    apk del tzdata && \
	sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories && \
    rm -rf /tmp/* /var/cache/apk/*
