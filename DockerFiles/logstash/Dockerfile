FROM docker.elastic.co/logstash/logstash:7.10.1
LABEL maintainer="Casey Smith"
RUN logstash-plugin install logstash-filter-translate
RUN rm -f /opt/logstash/pipeline/logstash.conf
add --chown=logstash:root ./logstash.conf /opt/logstash/pipeline/logstash.conf
add --chown=logstash:root  ./es.key /opt/logstash/config/es.key
add --chown=logstash:root  ./cisco.patterns /opt/logstash/patterns/cisco.patterns
add --chown=logstash:root  ./bigip-f5.patterns /opt/logstash/patterns/bigip-f5.patterns
RUN chmod 644 /opt/logstash/config/es.key
add --chown=logstash:root  ./es.crt /opt/logstash/config/es.crt
RUN chmod 644 /opt/logstash/config/es.crt
add --chown=logstash:root  ./chain.crt /opt/logstash/config/chain.crt
RUN chmod 644 /opt/logstash/config/chain.crt
