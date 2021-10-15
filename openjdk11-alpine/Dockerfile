FROM alpine:3.13.6
RUN adduser app -s /sbin/nologin --disabled-password
RUN  apk update \
  && apk upgrade \
  && apk add ca-certificates \
  && update-ca-certificates \
  && apk add --update coreutils && rm -rf /var/cache/apk/*   \ 
  && apk add --update openjdk11 curl \
  && apk add --no-cache nss \
  && rm -rf /var/cache/apk/*
USER app

