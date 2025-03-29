FROM ghcr.io/taffish-org/debian:12

LABEL maintainer="taffish@163.com"

WORKDIR /root

RUN apt-get update && apt-get install -y curl

RUN cd / && \
    curl -LO https://repo.anaconda.com/archive/Anaconda3-2024.10-1-Linux-$(uname -m).sh && \
    sh Anaconda3-2024.10-1-Linux-$(uname -m).sh -b && \
    rm Anaconda3-2024.10-1-Linux-$(uname -m).sh && \
    mv /root/anaconda3 /

ENV PATH=/anaconda3/bin:${PATH}

ENV TAFFISH_ENV=TAFFISH
ENV TAFFISH_NAME=conda
