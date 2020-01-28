# swarmstack/victoria-metrics

Docker compose file for [VictoriaMetrics](https://github.com/VictoriaMetrics/VictoriaMetrics): fast, cost-effective and scalable time series database, long-term remote storage for Prometheus

If you need to scale your metrics application even beyond the performance capabilities of VictoriaMetrics, see [Trickster](https://github.com/swarmstack/trickster) for an in-memory cache that can front-end VictoriaMetrics or Prometheus for possible further performance gains.

## USAGE

```
docker stack deploy -c docker-compose.yml victoria-metrics
```

[swarmstack](https://github.com/swarmstack/swarmstack) users should use docker-compose-swarmstack.yml above instead.

---

## Prometheus Config

```
remote_write:
  - url: http://victoria-metrics:8428/api/v1/write
```

Metrics from the VictoriaMetrics can optionally be scraped from the service URL http://victoria-metrics:8428/metrics
