ARG image=pihole/pihole:latest
ARG lan_domain
ARG lan_host

FROM ${image} AS pihole

RUN mkdir -p /etc/dnsmasq.d \
    && touch /etc/dnsmasq.d/05-wildcard.conf \
    && echo "address=/${lan_domain}/${lan_host}" > /etc/dnsmasq.d/05-wildcard.conf
