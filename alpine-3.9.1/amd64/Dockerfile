FROM scratch

ARG BUILD_DATE
ARG VCS_REF

LABEL maintainer="kuwork <kuwork@126.com>" \
    architecture="amd64/x86_64" \
    alpine-version="3.9.1" \
    build="25-Aug-2019" \
    org.opencontainers.image.title="alpine" \
    org.opencontainers.image.description="Docker image running on Alpine Linux" \
    org.opencontainers.image.authors="kuwork <kuwork@126.com>" \
    org.opencontainers.image.vendor="K.W. Systems" \
    org.opencontainers.image.version="v3.9.1" \
    org.opencontainers.image.url="https://hub.docker.com/r/kuwork/alpine/" \
    org.opencontainers.image.source="https://github.com/kuwork/alpine" \
    org.opencontainers.image.revision=$VCS_REF \
    org.opencontainers.image.created=$BUILD_DATE

ADD alpine-minirootfs-3.9.1-x86_64.tar.gz /
RUN cd / \
    && sed -i 's/dl-cdn.alpinelinux.org/mirrors.aliyun.com/g' /etc/apk/repositories
CMD ["/bin/sh"]
