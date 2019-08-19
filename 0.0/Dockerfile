FROM debian:buster 
COPY --from=theodus/idris2-ci-base:latest /root/.cabal/* /root/.cabal/* /usr/local/
RUN apt-get update && apt-get install -y \
  clang \
  chicken-bin racket \
  make \
  libtinfo5

env IDRIS_CC=clang
env PATH=$PATH:/usr/local/bin:/usr/local/etc:/usr/local/include:/usr/local/lib:/usr/local/sbin:/usr/local/share:/usr/local/src
cmd ["idris"]
