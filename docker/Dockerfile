FROM solr:8.11.1
ENV DEBIAN_FRONTEND=noninteractive

USER root
#RUN apt-get update && apt-get -y dist-upgrade
#RUN apt-get update && apt-get install -y mlocate sudo

#RUN echo "solr ALL=(root) NOPASSWD:ALL" > /etc/sudoers.d/solr && \
#    chmod 0440 /etc/sudoers.d/solr

RUN wget -P /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/ https://github.com/locationtech/jts/releases/download/jts-1.18.2/jts-core-1.18.2.jar
RUN wget -P /opt/solr/server/solr-webapp/webapp/WEB-INF/lib/ https://github.com/locationtech/jts/releases/download/jts-1.18.2/jts-io-common-1.18.2.jar

USER solr

ADD mmdconfig /opt/solr/server/solr/configsets/mmd

# RUN mkdir -p /var/solr/data/mmd && precreate-core  mmd /opt/solr/server/solr/configsets/mmd


RUN mkdir -p /tmp/data