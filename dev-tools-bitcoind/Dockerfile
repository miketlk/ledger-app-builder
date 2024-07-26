# An image derived from ledgerhq/ledger-app-builder/ledger-app-dev-tools but
# also containing the prebuilt bitcoin-core binaries obtained from the Alpine
# repository

FROM ghcr.io/ledgerhq/ledger-app-builder/ledger-app-dev-tools:latest

# Add packages
RUN apk upgrade -U && \
    apk --update --repository=http://dl-4.alpinelinux.org/alpine/edge/testing add \
    openssl wget ca-certificates bitcoin bitcoin-cli

# Add bitcoin binaries to path
ENV PATH=/bitcoin/bin:$PATH