FROM jenkins/jenkins:lts
MAINTAINER mariia markina <MariaMarkinaV@gmail.com>
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
#COPY default-user.groovy /usr/share/jenkins/ref/init.groovy.d/
COPY app_dev_ip.txt /usr/share/app_dev_ip.txt
COPY app_prod_ip.txt /usr/share/app_prod_ip.txt
ENV JAVA_OPTS="-Djenkins.install.runSetupWizard=false"
ENV JENKINS_USER admin
ENV JENKINS_PASS admin
#ENV JENKINS_OPTS="--argumentsRealm.roles.user=admin --argumentsRealm.passwd.admin=admin --argumentsRealm.roles.admin=admin"
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
ENTRYPOINT ["/sbin/tini", "--", "/usr/local/bin/jenkins.sh"]
