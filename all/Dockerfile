ARG VERSION_ID
FROM alpine:${VERSION_ID}

RUN source /etc/os-release && \
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-standard-${VERSION_ID}-x86_64.iso &&\
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-standard-${VERSION_ID}-x86_64.iso.sha256 && \
    sha256sum -c alpine-standard-${VERSION_ID}-x86_64.iso.sha256 && \
    rm alpine-standard-${VERSION_ID}-x86_64.iso.sha256

RUN source /etc/os-release && \
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-extended-${VERSION_ID}-x86_64.iso &&\
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-extended-${VERSION_ID}-x86_64.iso.sha256 && \
    sha256sum -c alpine-extended-${VERSION_ID}-x86_64.iso.sha256 && \
    rm alpine-extended-${VERSION_ID}-x86_64.iso.sha256

 RUN source /etc/os-release && \
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-virt-${VERSION_ID}-x86_64.iso &&\
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-virt-${VERSION_ID}-x86_64.iso.sha256 && \
    sha256sum -c alpine-virt-${VERSION_ID}-x86_64.iso.sha256 && \
    rm alpine-virt-${VERSION_ID}-x86_64.iso.sha256

 RUN source /etc/os-release && \
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-xen-${VERSION_ID}-x86_64.iso &&\
    wget -q https://dl-cdn.alpinelinux.org/alpine/v${VERSION_ID:0:4}/releases/x86_64/alpine-xen-${VERSION_ID}-x86_64.iso.sha256 && \
    sha256sum -c alpine-xen-${VERSION_ID}-x86_64.iso.sha256 && \
    rm alpine-xen-${VERSION_ID}-x86_64.iso.sha256