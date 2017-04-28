FROM openjdk:8-jre

WORKDIR /opt/scm-server/
ADD scm-server-*.tar.gz /opt/

RUN useradd -m scm && chown -R scm:scm /opt/scm-server/work

USER scm
EXPOSE 8080
VOLUME /home/scm/
CMD [ "/opt/scm-server/bin/scm-server"]
