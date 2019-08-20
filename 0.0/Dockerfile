FROM debian:bullseye

RUN apt-get update && apt-get install -y \
  netbase \
  zlib1g-dev \
  libncurses-dev \
  haskell-platform
  
RUN run cabal update && cabal install -j idris-1.3.2

RUN apt-get install -y \
  clang \
  chezscheme \
  chicken-bin racket \
  make

ENV PATH=$PATH:/usr/share/bin
ENV IDRIS_CC=clang
