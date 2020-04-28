# Get base image
FROM centos:7

# Author
MAINTAINER "Ngo Minh Phuong"

#Cai dat apache
RUN yum update -y
RUN yum install -y sudo
RUN yum install -y epel-release
RUN yum install -y http://rpms.remirepo.net/enterprise/remi-release-7.rpm
RUN yum clean all
RUN yum -y install wget
RUN yum -y install httpd
 
#Thiet lap thu muc lam viec 
WORKDIR /var/www/html

#copy code tu thu muc code vao image
COPY ./build/  /var/www/html/

# start httpd
CMD ["/usr/sbin/httpd", "-D", "FOREGROUND"]

EXPOSE 80
