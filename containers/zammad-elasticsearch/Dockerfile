FROM docker.elastic.co/elasticsearch/elasticsearch:7.16.2
ARG BUILD_DATE

LABEL org.label-schema.build-date="$BUILD_DATE" \
      org.label-schema.name="Zammad" \
      org.label-schema.license="AGPL-3.0" \
      org.label-schema.description="Docker container for Zammad - Elasticsearch" \
      org.label-schema.url="https://zammad.org" \
      org.label-schema.vcs-url="https://github.com/msatti/zammad" \
      org.label-schema.vcs-type="Git" \
      org.label-schema.vendor="Zammad" \
      org.label-schema.schema-version="5.0.3" \
      org.label-schema.docker.cmd="sysctl -w vm.max_map_count=262144;docker-compose up"

SHELL ["/bin/bash", "-e", "-o", "pipefail", "-c"]

RUN /usr/share/elasticsearch/bin/elasticsearch-plugin install --batch ingest-attachment
