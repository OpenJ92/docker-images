FROM ubuntu:24.04

ARG DEBIAN_FRONTEND=noninteractive
ARG WITH_PSQL=0

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    python3 python3-venv python3-pip \
    build-essential pkg-config \
 && rm -rf /var/lib/apt/lists/*

# Optional: psql client (not postgres server)
RUN if [ "$WITH_PSQL" = "1" ]; then \
      apt-get update && apt-get install -y --no-install-recommends postgresql-client && \
      rm -rf /var/lib/apt/lists/* ; \
    fi

ENV PYTHONDONTWRITEBYTECODE=1 \
    PYTHONUNBUFFERED=1

CMD ["bash"]
