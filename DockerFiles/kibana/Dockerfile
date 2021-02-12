FROM docker.elastic.co/kibana/kibana:7.10.1
LABEL maintainer="Casey Smith"
RUN rm -f /opt/kibana/config/kibana.yml
add --chown=kibana:root ./kibana.yml /opt/kibana/config/kibana.yml
add --chown=kibana:root  ./es.key /opt/kibana/config/kibana-server.key
RUN chmod 644 /opt/kibana/config/kibana-server.key
add --chown=kibana:root  ./es.crt /opt/kibana/config/kibana-server.crt
RUN chmod 644 /opt/kibana/config/kibana-server.crt
add --chown=kibana:root  ./chain.crt /opt/kibana/config/elasticsearch-ca.pem
RUN chmod 644 /opt/kibana/config/elasticsearch-ca.pem
