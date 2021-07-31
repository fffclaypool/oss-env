FROM centos:centos7
COPY . /app
WORKDIR /app
RUN yum update -y
RUN \
    yum install -y centos-release-scl \
    && yum install -y devtoolset-8 \
    && yum install -y git \
    && yum install -y libX11-devel \
    && yum install -y libXpm-devel \
    && yum install -y libXft-devel \
    && yum install -y libXext-devel \
    && yum install -y make \
    && yum install -y openssl-devel \
    && yum install -y scl-utils \
    && yum install -y wget \
    && yum install -y which
RUN scl enable devtoolset-8 bash
RUN \
    wget https://github.com/Kitware/CMake/releases/download/v3.21.1/cmake-3.21.1.tar.gz && \
    tar xvzf cmake-3.21.1.tar.gz && \
    cd cmake-3.21.1 && \
    ./bootstrap && \
    make -j 4 && \
    make install -j 4
ENV LC_ALL="en_US.UTF-8"
