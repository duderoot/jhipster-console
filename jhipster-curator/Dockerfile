FROM python:3.11-alpine3.17

RUN pip install  elasticsearch-curator && \
rm -rf /var/cache/apk/*

COPY ./config/ /config

RUN /usr/bin/crontab /config/crontab.txt

CMD ["/usr/sbin/crond","-f"]
