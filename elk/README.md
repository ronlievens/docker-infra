# Docker Compose file for an ELK stack

Start via the terminal `docker-compose up -d` and open:

- [Kibana Dashboard](http://127.0.0.1:5601/kibana)

## Documentation

- [Elasticsearch docker guide](https://www.elastic.co/guide/en/elasticsearch/reference/current/docker.html)
- [Logstash docker guide](https://www.elastic.co/guide/en/logstash/current/docker.html)
- [Kibana docker guide](https://www.elastic.co/guide/en/kibana/current/docker.html)
- [Docker hub at elastic](https://www.docker.elastic.co/)

## Health check

- [Elasticsearch health check](http://localhost:9200/_cat/health)
- [Logstash health check](http://localhost:9600/?pretty)
- [Kibana health check](http://127.0.0.1:5601/kibana/api/status)

## Setup named volumes

Create the name volumes with the following [commands](https://docs.docker.com/storage/volumes/):

Named volumes are stored in the folder:

- Windows: C:\ProgramData\Docker\volumes\
- Linux: /var/lib/docker/volumes/
- MacOS: /var/lib/docker/volumes/
