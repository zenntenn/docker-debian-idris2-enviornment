from debian:buster

run apt-get update && apt-get install -y \
  haskell-cabal-install \
  clang lld-4.0 \
  curl wget \
  chicken-bin racket \
  libx11-dev uuid-dev \
  libncurses5-dev

run cabal update && cabal install -j --with-ld=ld.lld-4.0 idris-1.3.2

env IDRIS_CC=clang
cmd idris
