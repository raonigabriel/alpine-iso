ARG VERSION_ID
FROM alpine:${VERSION_ID}

ARG VARIANT=standard

RUN source /etc/os-release && \
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-${VARIANT}-${VERSION_ID}-x86_64.iso &&\
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-${VARIANT}-${VERSION_ID}-x86_64.iso.sha256 && \
    sha256sum -c alpine-${VARIANT}-${VERSION_ID}-x86_64.iso.sha256 && \
    rm alpine-${VARIANT}-${VERSION_ID}-x86_64.iso.sha256