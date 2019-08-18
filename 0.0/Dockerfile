from debian:buster

run apt-get update && apt-get install -y \
  cabal-install \
  clang lld \
  curl wget \
  chicken-bin racket \
  libx11-dev uuid-dev \
  libncurses5-dev \
  zlib1g-dev

run cabal update && cabal install -j --with-ld=ld.lld idris-1.3.2

env IDRIS_CC=clang
cmd idris
