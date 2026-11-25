# Base image updated by Renovate, update versionCompatibility on Alpine base bump
ARG BUILD_FROM=ghcr.io/home-assistant/base:3.24-2026.11.1@sha256:5021aac8a4b7f2a1397e23a9749dfe9f736463ffa471df6b200216c68d530fe6
FROM $BUILD_FROM

# Add env
ENV LANG=C.UTF-8

# Setup base
RUN apk add --no-cache samba-common-tools samba-common

# Copy data
COPY data/run.sh /

CMD [ "/run.sh" ]

LABEL \
    org.opencontainers.image.title="Home Assistant App: RPC Shutdown" \
    org.opencontainers.image.description="Shutdown Windows machines remotely" \
    org.opencontainers.image.source="https://github.com/home-assistant/app-rpc-shutdown" \
    org.opencontainers.image.licenses="Apache License 2.0"
