# Dockerfile

rabbitmq 添加插件delayed_message

官网下载好delayed_message插件后

编辑Dockerfile：

#vim Dockerfile
From rabbitmq:3-management
COPY rabbitmq_delayed_message_exchange-20171201-3.7.x.ez /plugins
RUN rabbitmq-plugins enable --offline rabbitmq_delayed_message_exchange

#构建镜像即可~
#docker build -t rabbitmq:3-management-delayed .
