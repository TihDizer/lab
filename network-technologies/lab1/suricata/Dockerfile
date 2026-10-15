FROM ubuntu:24.04

ENV DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        software-properties-common \
        ca-certificates \
        curl \
        jq \
        iproute2 \
        iptables \
        libnetfilter-queue1 \
        libnfnetlink0 \
        libcap2-bin && \
    add-apt-repository -y ppa:oisf/suricata-stable && \
    apt-get update && \
    apt-get install -y --no-install-recommends suricata && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir -p /etc/suricata/rules /var/log/suricata

CMD ["suricata", "-c", "/etc/suricata/suricata.yaml", "-q", "1"]
