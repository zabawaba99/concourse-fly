FROM alpine:3.8

ENTRYPOINT [ "fly" ]

ENV \
    PATH=/usr/local/bin:$PATH \
    CONCOURSE_VERSION=v3.14.1

RUN apk add --no-cache ca-certificates && \
    wget -O /tmp/fly https://github.com/concourse/concourse/releases/download/${CONCOURSE_VERSION}/fly_linux_amd64 && \
    mv /tmp/fly /usr/local/bin/fly && \
    chmod +x /usr/local/bin/fly
