FROM docker.elastic.co/logstash/logstash:5.6.9
RUN rm -f /usr/share/logstash/pipeline/logstash.conf
ADD pipeline/logstash.conf /usr/share/logstash/pipeline/logstash.conf
ADD config/logstash.yml /usr/share/logstash/config/logstash.yml