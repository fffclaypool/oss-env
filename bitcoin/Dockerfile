FROM ubuntu:18.04
COPY . /app
WORKDIR /app
RUN apt-get update
RUN \
    apt-get install -y \
        build-essential \
        libtool \
        autotools-dev \
        automake \
        pkg-config \
        bsdmainutils \
        python3 \
        libevent-dev \
        libboost-dev \
        libboost-system-dev \
        libboost-filesystem-dev \
        libboost-test-dev \
        libzmq3-dev \
        libqt5gui5 \
        libqt5core5a \
        libqt5dbus5 \
        qttools5-dev \
        qttools5-dev-tools \
        libqrencode-dev
RUN \
    apt install -y \
        git \
        libsqlite3-dev \
        libminiupnpc-dev \
        libnatpmp-dev
