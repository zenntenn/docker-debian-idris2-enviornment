FROM debian:bullseye-slim

ARG stack_yaml
ADD $stack_yaml ./

RUN apt-get update && apt-get install -y \
            haskell-platform \
            haskell-stack \
            clang llvm \
            chezscheme \
            racket \
            libx11-dev uuid-dev \
            libncurses5-dev \ 
            build-essential pkg-config libffi-dev libgmp-dev && \
    stack install idris-1.3.2

ENV PATH="${HOME}/bin;/bin/jdk/bin:/bin/idris-jvm/codegen/bin:${PATH}"
ENV IDRIS_CC=clang

CMD idris
