FROM docker.elastic.co/elasticsearch/elasticsearch:7.10.1
LABEL maintainer="Casey Smith"
add --chown=elasticsearch:root ./es.crt /usr/share/elasticsearch/config/es.crt
add --chown=elasticsearch:root ./es.key /usr/share/elasticsearch/config/es.key
add --chown=elasticsearch:root ./chain.crt /usr/share/elasticsearch/config/ca.crt
RUN chmod 644 /usr/share/elasticsearch/config/ca.crt
RUN chmod 644 /usr/share/elasticsearch/config/es.crt
RUN chmod 644 /usr/share/elasticsearch/config/es.key
