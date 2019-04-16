From meimeidebiaobiao/alpine
MAINTAINER meimeidebiaobiao

WORKDIR /home/svn

RUN apk update && \
    apk add --no-cache subversion

CMD [ "/usr/bin/svnserve", "--daemon", "--foreground", "--root", "/home/svn" ]
