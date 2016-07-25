FROM alpine:latest

MAINTAINER Gustavo Marttos <marttosc@gmail.com>

RUN apk add --update curl && \
    rm -rf /var/cache/apk/*

RUN curl -O http://cli.exercism.io/install
RUN chmod +x install
RUN DIR=/usr/local/bin ./install

ENTRYPOINT ["exercism"]

