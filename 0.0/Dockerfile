FROM debian:buster 
COPY --from=theodus/idris2-ci-base:latest /root/.cabal/bin/* /usr/bin/
RUN apt-get update && apt-get install -y \
  clang \
  chicken-bin racket \
  make \
  libtinfo5

env IDRIS_CC=clang
cmd ["idris"]
