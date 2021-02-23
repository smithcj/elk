FROM docker.elastic.co/beats/filebeat:7.11.1
LABEL maintainer="Casey Smith"
RUN mv  /usr/share/filebeat/modules.d/netflow.yml.disabled  /usr/share/filebeat/modules.d/netflow.yml.old
add --chown=filebeat:root ./netflow.yml  /usr/share/filebeat/modules.d/netflow.yml 
RUN chmod 644 /usr/share/filebeat/modules.d/netflow.yml
add --chown=filebeat:root  ./es.key /cert.key
RUN chmod 644 /cert.key
add --chown=filebeat:root  ./es.crt /cert.pem
RUN chmod 644 /cert.pem
add --chown=filebeat:root  ./chain.crt /ca.pem
RUN chmod 644 /ca.pem
COPY filebeat.docker.yml /usr/share/filebeat/filebeat.yml
USER root
RUN chown root:filebeat /usr/share/filebeat/filebeat.yml
USER filebeat
