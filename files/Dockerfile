FROM jenkins/jenkins:lts
MAINTAINER mariia markina <MariaMarkinaV@gmail.com>
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
