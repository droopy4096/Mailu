FROM alpine:edge

RUN echo "@testing http://nl.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories \
 && apk add --no-cache rmilter@testing rsyslog bash

COPY rmilter.conf /etc/rmilter.conf
COPY rmilter-clamav.conf /etc/rmilter-clamav.conf
COPY rsyslog.conf /etc/rsyslog.conf

COPY start.sh /start.sh

CMD ["/start.sh"]
