FROM alpine:latest

MAINTAINER Gustavo Marttos <marttosc@gmail.com>

ARG API_KEY

RUN apk add --update curl && \
    rm -rf /var/cache/apk/*

RUN curl -O http://cli.exercism.io/install
RUN chmod +x install
RUN DIR=/usr/local/bin ./install

RUN exercism configure --dir=/opt/exercism
RUN exercism configure --key=${API_KEY}

ENTRYPOINT ["exercism"]

