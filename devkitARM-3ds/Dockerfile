FROM greatwizard/devkitarm
MAINTAINER Guillaume Gérard "guillaume.gerard88@gmail.com"

RUN apt-get update && \
  apt-get install -y \
    git && \
  rm -rf /var/lib/apt/lists/*

WORKDIR /opt/devkitPro
RUN git clone --depth=1 https://github.com/smealum/ctrulib.git && \
  git clone --depth=1 https://github.com/fincs/citro3d.git

WORKDIR /opt/devkitPro/ctrulib/libctru
RUN make && \
  make install

WORKDIR /opt/devkitPro/citro3d
RUN make && \
  make install

WORKDIR /source
CMD ["bash"]
