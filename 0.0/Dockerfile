from haskell:8.2

run apt-get update && apt-get install -y \
  clang lld-4.0 \
  curl wget \
  chicken-bin racket \
  libx11-dev uuid-dev \
  libncurses5-dev
  
run echo "deb http://ftp.debian.org/debian stretch-backports main contrib non-free" > /etc/apt/sources.list.d/backports.list && \
  apt-get update && apt-get -t stretch-backports -y install chezscheme
  
run cabal update && cabal install -j --with-ld=ld.lld-4.0 --bindir /usr/bin idris-1.3.2

env IDRIS_CC=clang
cmd idris
