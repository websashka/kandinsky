FROM nginx

RUN apt-get update && \
    apt-get install -y tor supervisor && \
    apt-get clean && rm -rf /var/lib/apt/lists/*

COPY nginx.conf /etc/nginx/conf.d/default.conf
COPY supervisord.conf /etc/supervisor/conf.d/supervisord.conf
COPY torrc /etc/tor/torrc

VOLUME /var/www/html
VOLUME /var/lib/tor/

CMD ["/usr/bin/supervisord"]
