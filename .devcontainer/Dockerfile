FROM mcr.microsoft.com/vscode/devcontainers/base:0-ubuntu-20.04
# Erlang Solutions repository
RUN wget -q https://packages.erlang-solutions.com/erlang-solutions_2.0_all.deb && \
    dpkg -i erlang-solutions_2.0_all.deb && \
    rm erlang-solutions_2.0_all.deb
# Additional packages
RUN apt-get update && \
    export DEBIAN_FRONTEND=noninteractive && \
    apt-get install -y --no-install-recommends \
        elixir=1.13.4-1 \
        erlang=1:25.0.4-1 \
        inotify-tools=3.14-8 \
        postgresql-client=12+214ubuntu0.1 \
        tig=2.4.1-1ubuntu1 && \
    apt-get autoremove -y && \
    apt-get clean -y && \
    rm -rf /var/lib/apt/lists/*
