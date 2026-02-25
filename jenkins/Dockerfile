FROM jenkins:alpine

RUN /usr/local/bin/install-plugins.sh pipeline-stage-view workflow-multibranch git maven sonar blueocean credentials-binding matrix-auth

ENV JENKINS_USER admin
ENV JENKINS_PASS admin

# Skip initial setup
ENV JAVA_OPTS -Djenkins.install.runSetupWizard=false

COPY default-user.groovy /usr/share/jenkins/ref/init.groovy.d/


COPY ./maven /opt/maven
