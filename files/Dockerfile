FROM jenkins/jenkins:lts
MAINTAINER mariia markina <MariaMarkinaV@gmail.com>
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
ENV JENKINS_USER admin
ENV JENKINS_PASS admin
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
