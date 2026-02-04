# docker-images

Toolchain-focused base images (no editor, no git). Optional `psql` client via build arg.

## Build

### Python
`docker build -t jmvs/py:latest images/py`
docker build -t jmvs/py:psql --build-arg WITH_PSQL=1 images/py

### Haskell
docker build -t jmvs/haskell:latest images/haskell
docker build -t jmvs/haskell:psql --build-arg WITH_PSQL=1 images/haskell

### C
docker build -t jmvs/c:latest images/c
docker build -t jmvs/c:psql --build-arg WITH_PSQL=1 images/c

### Agda
docker build -t jmvs/agda:latest images/agda
docker build -t jmvs/agda:psql --build-arg WITH_PSQL=1 images/agda

### Polyglot
docker build -t jmvs/polyglot:latest images/polyglot
docker build -t jmvs/polyglot:psql --build-arg WITH_PSQL=1 images/polyglot

## Run
docker run -it --rm jmvs/py:latest
# docker-images
