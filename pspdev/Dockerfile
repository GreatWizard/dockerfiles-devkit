FROM debian:buster

LABEL maintainer="Guillaume Gérard <guillaume.gerard88@gmail.com>"

ENV DEBIAN_FRONTEND="noninteractive"

ENV PSPDEV /usr/local/pspdev
ENV PATH ${PATH}:${PSPDEV}/bin

RUN apt-get update && apt-get install -y \
  git \
  autoconf \
  automake \
  bison \
  bzip2 \
  cmake \
  doxygen \
  flex \
  gettext \
  g++ \
  gcc \
  git \
  gzip \
  libarchive-dev \
  libcurl4-openssl-dev \
  libelf-dev \
  libgpgme-dev \
  libncurses5-dev \
  libreadline-dev \
  libssl-dev \
  libtool-bin \
  libusb-dev \
  m4 \
  make \
  patch \
  pkg-config \
  python3 \
  python3-venv \
  subversion \
  tar \
  tcl \
  texinfo \
  unzip \
  wget \
  xz-utils \
  && rm -rf /var/lib/apt/lists/*

RUN git clone https://github.com/pspdev/psptoolchain.git && \
  cd psptoolchain && ./toolchain.sh && cd .. && \
  rm -Rf psptoolchain

RUN mkdir /source
WORKDIR /source
CMD ["bash"]
