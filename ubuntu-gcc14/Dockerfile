FROM gcc:14.2.0

FROM ubuntu:oracular-20240617

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN apt update && \
    apt install build-essential -y && \
    apt install wget tar file -y && \
    apt install libmpfr-dev libgmp3-dev libmpc-dev -y

RUN wget http://ftp.gnu.org/gnu/gcc/gcc-14.1.0/gcc-14.1.0.tar.gz && \
    tar -xf gcc-14.1.0.tar.gz && \
    cd gcc-14.1.0 && \
    ./configure -v --build=x86_64-linux-gnu --prefix=/usr/local/gcc-14.1.0 --enable-languages=c --disable-multilib --program-suffix=-14.1.0 && \
    make -j`nproc --ignore=2` && \
    make install
