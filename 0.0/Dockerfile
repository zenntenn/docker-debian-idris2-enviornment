FROM debian:Bullseye
RUN apt-get update && apt-get install -y \
  clang \
  chicken-bin racket \
  make \
  haskell-stack
RUN stack install idris --local-bin-path /usr/share/bin --resolver=lts-12

ENV PATH=$PATH:/usr/share/bin
ENV IDRIS_CC=clang
