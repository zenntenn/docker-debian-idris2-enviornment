FROM debian:bullseye

RUN apt-get update && apt-get install -y \
  netbase \
  zlib1g-dev \
  libncurses-dev \
  haskell-stack
  
RUN stack upgrade --binary-only

RUN stack install idris --local-bin-path /usr/share/bin --stack-yaml ./stack.yaml

RUN apt-get install -y \
  clang \
  chezscheme \
  chicken-bin racket \
  make

ENV PATH=$PATH:/usr/share/bin
ENV IDRIS_CC=clang
