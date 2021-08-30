FROM ubuntu

RUN true \
    && apt update \
    && apt install -y \
        wget

WORKDIR /app

RUN wget https://github.com/prometheus/node_exporter/releases/download/v1.2.2/node_exporter-1.2.2.linux-amd64.tar.gz

RUN true \
    && tar -xvzf node_exporter-1.2.2.linux-amd64.tar.gz \
    && mv node_exporter-1.2.2.linux-amd64/node_exporter . \
    && rm -Rfv node_exporter-1.2.2.linux-amd64*

ENTRYPOINT [ "/app/node_exporter" ]