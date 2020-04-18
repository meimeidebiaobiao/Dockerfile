FROM meimeidebiaobiao/alpine
MAINTAINER meimeidebiaobiao
RUN apk update && \
    apk add --no-cache mysql-client && \
    apk del tzdata && \
    rm -rf /tmp/* /var/cache/apk/*