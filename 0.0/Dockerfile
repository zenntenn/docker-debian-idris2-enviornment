FROM mmhelloworld/idris:1.3.2

RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list \
            apt-get update \
            apt-get -t stretch-backports install chezscheme \
            apt-get install -y \
            clang llvm \
            racket \
            libx11-dev uuid-dev \
            libncurses5-dev \ 
            build-essential pkg-config libffi-dev libgmp-dev && \
    stack install idris-1.3.2

ENV PATH="${HOME}/bin:${PATH}"
ENV IDRIS_CC=clang
