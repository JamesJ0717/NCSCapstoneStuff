ARG ELK_VERSION

FROM docker.elastic.co/beats/metricbeat:${ELK_VERSION}

COPY --chown=root:metricbeat ./config/metricbeat.yml metricbeat.yml

USER root