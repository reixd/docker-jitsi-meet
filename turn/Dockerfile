ARG VERSION
FROM instrumentisto/coturn:${VERSION:-latest}

RUN apk add --no-cache openssl
RUN apk add --no-cache certbot
RUN apk add --no-cache bash

COPY rootfs/ /

ENTRYPOINT ["/docker-entrypoint.sh"]

VOLUME ["/config"]

EXPOSE 5349 8443 10000:11000/udp

