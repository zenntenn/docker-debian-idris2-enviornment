from haskell:8.2

run echo "deb http://ftp.debian.org/debian stretch-backports main contrib non-free" | sudo tee /etc/apt/sources.list.d/backports.list \
  apt-get update && apt-get install -y \
  clang lld-4.0 \
  curl wget \
  chicken-bin racket \
  libx11-dev uuid-dev \
  libncurses5-dev \
  apt-get -t stretch-backports install chezscheme
  
run cabal update && cabal install -j --with-ld=ld.lld-4.0 --bindir /usr/bin idris-1.3.2

env IDRIS_CC=clang
cmd idris
