FROM centos:latest

RUN yum -y install createrepo epel-release firewalld rsync && \
    yum -y install nginx && \
    yum clean all

ADD nginx.conf  /etc/nginx/nginx.conf
ADD repo.conf   /etc/nginx/conf.d/repo.conf
ADD update_repo /usr/local/sbin/update_repo

EXPOSE 80
VOLUME /var/www/html/repos

CMD ["nginx", "-g", "daemon off;"]
