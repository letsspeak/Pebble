FROM swift:4.1
LABEL maintainer="letsspeak"

# Install curl & jq
RUN apt-get update && \
    apt-get -y install curl jq && \
    rm -rf /var/lib/apt/lists/*;

WORKDIR /var/pebble
