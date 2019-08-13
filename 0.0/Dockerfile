FROM mrlsd/idris:1.3.2

RUN echo 'deb http://deb.debian.org/debian stretch-backports main' > /etc/apt/sources.list.d/backports.list \
            apt-get update \
            apt-get -t stretch-backports install chezscheme \
            apt-get install -y clang llvm racket bash
            
ENV PATH="${HOME}/bin:${PATH}"
ENV IDRIS_CC=clang
CMD idris
