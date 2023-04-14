# Docker Compose file for Prometheus

Start via the terminal `docker-compose up -d` and open:

- [Prometheus Dashboard](http://127.0.0.1:9090/prometheus/)

## Documentation

- [Spring Boot Actuator metrics monitoring with Prometheus and Grafana](https://www.callicoder.com/spring-boot-actuator-metrics-monitoring-dashboard-prometheus-grafana/)
- [Prometheus CLI options](https://gist.github.com/0x0I/eec137d55a26a16d836b84cbc186ab52#file-prometheus-cli-options-L18)
- [Prometheus MANAGEMENT API](https://prometheus.io/docs/prometheus/latest/management_api/)
- [Docker hub - Prometheus](https://hub.docker.com/r/prom/prometheus/)

## Health check

- [Prometheus health check](http://localhost:9090/-/healthy)

## example prometheus.yml

The `host.docker.internal` is to connect to the `localhost` from a docker image.

```yaml
scrape_configs:
    - job_name: 'Spring boot example on localhost'
      metrics_path: '/api/actuator/prometheus'
      scrape_interval: 5s
      static_configs:
          - targets: [ 'host.docker.internal:8080' ]
    - job_name: 'Golang with Echo example on localhost'
      metrics_path: '/metrics'
      scrape_interval: 5s
      static_configs:
          - targets: [ 'host.docker.internal:1323' ]
 
```
