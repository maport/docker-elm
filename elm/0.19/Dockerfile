FROM alpine:3.10.3

MAINTAINER Michael Porter <mike@codesimple.net>

RUN wget -O - 'https://github.com/elm/compiler/releases/download/0.19.1/binary-for-linux-64-bit.gz' \
    | gunzip -c >/usr/local/bin/elm
RUN chmod +x /usr/local/bin/elm

ENTRYPOINT ["elm"]
