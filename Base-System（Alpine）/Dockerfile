FROM Alpine

RUN apk update && \
    apk add --no-cache busybox-extras curl busybox tzdata && \
    cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo Asia/Shanghai > /etc/timezone && \
    apk del tzdata && \
    rm -rf /tmp/* /var/cache/apk/*