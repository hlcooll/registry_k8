FROM alpine:3.9

MAINTAINER hualei 834890137@qq.com
WORKDIR /usr/local/bin
#修改阿里云
COPY repositories /etc/apk/repositories
#apk 包
RUN apk add --no-cache bash wget curl git make vim tzdata gcc musl-dev 
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime
RUN echo "Asia/Shanghai" > /etc/timezone
#清理包
RUN apk del bash wget curl git make vim tzdata gcc musl-dev
RUN rm -rf /var/cache/apk/* 
