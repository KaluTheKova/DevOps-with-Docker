FROM alpine:3.15

RUN apk add --no-cache bash

# Building
WORKDIR /usr/src/midi-sorter
COPY . .
RUN ls

ENTRYPOINT [ "bash" ]