FROM bitnami/prometheus:latest

WORKDIR app/

COPY prometheus.yml .

CMD ["--config.file=prometheus.yml"]