FROM zt/alpine:v1

MAINTAINER hualei 834890137@qq.com
#安装 go 环境
ADD go1.10.3.linux-amd64.tar.gz /usr/local
WORKDIR /usr/local
RUN apk --no-cache add ca-certificates wget \
    &&wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub
COPY glibc-2.29-r0.apk /usr/local
RUN apk add glibc-2.29-r0.apk
RUN rm -rf glibc-2.29-r0.apk
ENV GOROOT=/usr/local/go 
ENV PATH=$PATH:$GOROOT/bin 
ENV GOPATH=/opt



