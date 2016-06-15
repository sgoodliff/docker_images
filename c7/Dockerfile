FROM centos:7
MAINTAINER "Steven Goodliff" <sgoodliff@gmail.com>
ENV container docker

RUN yum -y install httpd php php-devel; yum clean all
RUN echo "The Web Server is Running Today" > /var/www/html/index.html
RUN echo "<?php phpinfo(); ?>" > /var/www/html/phpinfo.php
EXPOSE 80

# Start the service
CMD ["-D", "FOREGROUND"]
ENTRYPOINT ["/usr/sbin/httpd"]
