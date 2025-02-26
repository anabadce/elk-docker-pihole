FROM docker.elastic.co/logstash/logstash:8.17.2

COPY config/logstash.yml /usr/share/logstash/config/
COPY pipeline/* /usr/share/logstash/pipeline/
COPY patterns/dns /usr/share/logstash/patterns/

# PiHole: changing logstash group to 1001 to allow read pihole log, matching host's PiHole group
USER 1000:1001
