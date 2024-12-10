FROM hexpm/elixir:1.17.3-erlang-26.1.2-debian-bookworm-20241111-slim as dev

# install build dependencies
# --allow-releaseinfo-change allows to pull from 'oldstable'
RUN apt-get update --allow-releaseinfo-change -y && \
    apt-get install -y \
    build-essential \
    git \
    openssl \
    erlang-dev \
    ca-certificates \
    inotify-tools && \
    apt-get clean && \
    rm -f /var/lib/apt/lists/*_*

# Install hex
RUN mix local.hex --force && \
    mix local.rebar --force && \
    mix hex.info

WORKDIR /src