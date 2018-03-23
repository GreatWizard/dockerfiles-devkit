FROM greatwizard/devkitarm
MAINTAINER Guillaume Gérard "guillaume.gerard88@gmail.com"

ENV VITASDK /usr/local/vitasdk
ENV PATH $VITASDK/bin:$PATH

RUN apt-get update && \
  apt-get install -y \
    cmake \
    git && \
  rm -rf /var/lib/apt/lists/*

WORKDIR /opt
RUN git clone https://github.com/vitasdk/vdpm

WORKDIR /opt/vdpm
RUN ./bootstrap-vitasdk.sh && \
  ./install-all.sh

WORKDIR /source
CMD ["bash"]
