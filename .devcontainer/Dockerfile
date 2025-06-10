FROM alpine:latest

# Install glibc using sgerrand's package repository
RUN apk add --no-cache wget ca-certificates \
    && wget -q -O /etc/apk/keys/sgerrand.rsa.pub https://alpine-pkgs.sgerrand.com/sgerrand.rsa.pub \
    && GLIBC_VERSION=2.37-r0 \
    && wget -q https://github.com/sgerrand/alpine-pkg-glibc/releases/download/${GLIBC_VERSION}/glibc-${GLIBC_VERSION}.apk \
    && apk add --no-cache glibc-${GLIBC_VERSION}.apk \
    && rm glibc-${GLIBC_VERSION}.apk
