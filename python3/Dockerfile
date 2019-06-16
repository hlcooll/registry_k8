FROM zt/alpine:v1

MAINTAINER hualei 834890137@qq.com
#安装python3
RUN apk add --no-cache python3
RUN apk add --no-cache musl-dev
#pip安装
COPY get-pip.py /tmp
RUN cd /tmp \
    &&python3 get-pip.py
#python3改python
RUN ln -sf /usr/bin/python3 /usr/bin/python

