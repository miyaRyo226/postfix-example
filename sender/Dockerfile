FROM debian:bullseye-slim
WORKDIR /root
RUN DEBIAN_FRONTEND=noninteractive apt-get update && apt-get install -y \
    postfix \
    rsyslog \
    && rm -rf /var/lib/apt/lists/*
RUN cp /etc/services /var/spool/postfix/etc/
CMD ["/bin/bash","-c","cp /etc/resolv.conf /var/spool/postfix/etc/resolv.conf && postfix start-fg"]