Dit project bestaat uit ELK, MailHog, Prometheus, Grafana, Jaeger docker compose files om een snelle start te geven aan een ontwikkelaar. 

# Dashboards

- [Kibana Dashboard](http://127.0.0.1:5601/kibana/)
- [MailHog Dashboard](http://127.0.0.1:9025/mailhog/)
- [Prometheus Dashboard](http://127.0.0.1:9090/prometheus/)
- [Grafana Dashboard](http://127.0.0.1:3000/grafana/)
- [Jaeger Dashboard](http://127.0.0.1:16686/jaeger/)

# Docker - use bash
Start all

```shell
docker-compose -f elk/docker-compose.yaml up -d
docker-compose -f mailhog/docker-compose.yaml up -d
docker-compose -f prometheus/docker-compose.yaml up -d
docker-compose -f grafana/docker-compose.yaml up -d
docker-compose -f jaeger/docker-compose.yaml up -d
```

Stop all

```shell
docker-compose -f elk/docker-compose.yaml down
docker-compose -f mailhog/docker-compose.yaml down
docker-compose -f prometheus/docker-compose.yaml down
docker-compose -f grafana/docker-compose.yaml down
docker-compose -f jaeger/docker-compose.yaml down
```

Show all containers running

```shell
docker ps
```

Remove all containers

```shell
docker rm -f $(docker ps -aq)
```

Remove all images

```shell
docker rmi -f $(docker images -qa)
```

Remove volumes

````shell
docker volume rm $(docker volume ls -q)
````
