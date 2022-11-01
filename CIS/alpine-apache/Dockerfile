FROM alpine:3.16.2
RUN apk add apache2 \
    && rc-service apache2 start \
    && rc-update add apache2