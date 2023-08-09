FROM ubuntu:jammy

LABEL org.opencontainers.image.authors="AnHeuermann"

# Ensure DEBIAN_FRONTEND is only set during build
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get upgrade -qy && apt-get dist-upgrade -qy
RUN apt-get install -qy \
  ca-certificates       \
  curl                  \
  gnupg

RUN apt-get install -qy cmake flex build-essential

# Clean
RUN rm -rf /var/lib/apt/lists/* \
  && apt-get clean
