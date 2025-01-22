FROM ubuntu:20.04
# Install required packages - g++ make, boost-devel, pthread
ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && apt-get install -y \
    g++ \
    make \
    libboost-all-dev \
    wget

RUN apt-get install -y libpthread-stubs0-dev 

RUN wget https://github.com/Adrian-Cantu/PRINSEQ-plus-plus/releases/download/v1.2.4/binary_prinseq-plus-plus-1.2.4.tar.gz \
    && tar -xvzf binary_prinseq-plus-plus-1.2.4.tar.gz \
    && mv prinseq++ /usr/local/bin/ 

ENTRYPOINT ["/usr/local/bin/prinseq++"]