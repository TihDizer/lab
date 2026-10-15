FROM kalilinux/kali-rolling:latest

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
        curl \
        iputils-ping && \
    rm -rf /var/lib/apt/lists/*

CMD ["sleep", "infinity"]
