FROM docker.elastic.co/logstash/logstash:6.4.1

RUN yum install -y unzip

RUN logstash-plugin install logstash-filter-jdbc_streaming
RUN logstash-plugin install logstash-filter-aggregate
RUN logstash-plugin install logstash-input-jdbc
RUN logstash-plugin install logstash-output-mongodb

COPY ./jars /logstash/jars
ENTRYPOINT ["/docker-entrypoint.sh"]
CMD ["-e", ""]
