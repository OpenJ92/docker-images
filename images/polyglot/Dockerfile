FROM ubuntu:24.04

ARG DEBIAN_FRONTEND=noninteractive
ARG WITH_PSQL=0

RUN apt-get update && apt-get install -y --no-install-recommends \
    ca-certificates \
    # Python
    python3 python3-venv python3-pip \
    # C/C++
    build-essential pkg-config clang gdb lldb cmake ninja-build make \
    # Haskell / Agda
    ghc cabal-install \
    libgmp-dev zlib1g-dev libffi-dev \
    agda agda-stdlib \
 && rm -rf /var/lib/apt/lists/*

RUN if [ "$WITH_PSQL" = "1" ]; then \
      apt-get update && apt-get install -y --no-install-recommends postgresql-client && \
      rm -rf /var/lib/apt/lists/* ; \
    fi

CMD ["bash"]

