FROM docker.io/ubuntu:22.04 AS builder

WORKDIR /app

# Install Python and git
RUN apt-get update && \
    apt-get install -y git python3 python3-venv --no-install-recommends && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/* && \
    python3 -m venv env

RUN /app/env/bin/pip install gunicorn

RUN git clone https://github.com/florianfesti/boxes.git /app/boxes
WORKDIR /app/boxes
RUN /app/env/bin/pip install .

CMD ["/app/env/bin/python3", "/app/boxes/scripts/boxesserver"]
