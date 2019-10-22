FROM jenkinsci/blueocean

ARG user=jenkins
ARG docker_group=docker
ARG docker_gid=993

USER root
RUN apk add --no-cache shadow
RUN groupmod -g ${docker_gid} ${docker_group} \
  && usermod -a -G ${docker_group} ${user}

USER ${user}
COPY plugins.txt /usr/share/jenkins/ref/plugins.txt
RUN /usr/local/bin/install-plugins.sh < /usr/share/jenkins/ref/plugins.txt
