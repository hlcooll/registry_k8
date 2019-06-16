FROM zt/alpine:v1

MAINTAINER hualei 834890137@qq.com
#安装jdk1.8
RUN mkdir -p /usr/java
ADD jdk-8u192-linux-x64.tar.gz /usr/java/
WORKDIR /usr/java
RUN apk --no-cache add ca-certificates wget \
    &&wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub
COPY glibc-2.29-r0.apk /usr/java
RUN apk add glibc-2.29-r0.apk
RUN rm -rf glibc-2.29-r0.apk
ENV JAVA_HOME=/usr/java/jdk1.8.0_192        
ENV JRE_HOME=/usr/java/jdk1.8.0_192/jre     
ENV CLASS_PATH=.:$JAVA_HOME/lib/dt.jar:$JAVA_HOME/lib/tools.jar:$JRE_HOME/lib
ENV PATH=$PATH:$JAVA_HOME/bin:$JRE_HOME/bin

RUN rm -rf glibc-2.29-r0.apk

CMD ["java"," -version"]