FROM zt/alpine:v1

MAINTAINER hualei 834890137@qq.com
WORKDIR /app
VOLUME /app
COPY startup.sh /startup.sh
RUN chmod +x /startup.sh 
RUN apk add --update mysql mysql-client && rm -f /var/cache/apk/*
COPY my.cnf /etc/my.cnf

EXPOSE 3306
CMD ["/startup.sh"]
