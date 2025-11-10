FROM debian:bookworm-slim

ENV DEBIAN_FRONTEND=noninteractive
SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    curl \
    bash \
    nano \
    net-tools \
    python3 \
    python3-pip \
    openssh-client \
    dnsutils \
    bash-completion \
    git \
    && apt-get clean && rm -rf /var/lib/apt/lists/*

RUN curl -s https://ludus.cloud/install -o /tmp/ludus-install.sh \
    # force completions_response to y
    && sed -i 's/\(read .*completions_response.*\)/completions_response="y"/' /tmp/ludus-install.sh \
    && bash /tmp/ludus-install.sh

# add completions to bashrc
RUN echo "source /usr/share/bash-completion/completions/ludus" >> .bashrc

ENV PATH="/usr/local/bin:${PATH}"
