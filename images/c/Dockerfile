FROM ubuntu:24.04

ARG DEBIAN_FRONTEND=noninteractive
ARG WITH_PSQL=0

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    build-essential pkg-config \
    clang gdb lldb \
    cmake ninja-build make \
 && rm -rf /var/lib/apt/lists/*

RUN if [ "$WITH_PSQL" = "1" ]; then \
      apt-get update && apt-get install -y --no-install-recommends postgresql-client && \
      rm -rf /var/lib/apt/lists/* ; \
    fi

CMD ["bash"]

