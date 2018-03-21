FROM greatwizard/devkitarm
MAINTAINER Guillaume Gérard "guillaume.gerard88@gmail.com"

RUN apt-get update && \
  apt-get install -y \
    unzip \
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

RUN wget https://github.com/dnasdw/3dstool/releases/download/v1.1.1/3dstool_linux_x86_64.tar.gz -O 3dstool.tar.gz && \
  tar xf 3dstool.tar.gz -C /usr/local/bin && \
  rm 3dstool.tar.gz

RUN wget https://github.com/devkitPro/3dstools/releases/download/v1.1.2/3dstools-1.1.2-x86_64-linux.tar.bz2 -O 3dsxtool.tar.bz2 && \
  tar xf 3dsxtool.tar.bz2 -C /usr/local/bin && \
  rm 3dsxtool.tar.bz2

RUN wget https://github.com/Steveice10/bannertool/releases/download/1.1.0/bannertool.zip -O bannertool.zip && \
  unzip bannertool.zip -d bannertool && \
  mv bannertool/linux-x86_64/bannertool /usr/local/bin && \
  rm -rf bannertool bannertool.zip

RUN wget https://github.com/profi200/Project_CTR/releases/download/0.15/makerom_015_ctrtool.zip -O makerom_ctrtool.zip && \
  unzip makerom_ctrtool.zip -d makerom_ctrtool && \
  mv makerom_ctrtool/Linux_x86_64/makerom /usr/local/bin && \
  mv makerom_ctrtool/Linux_x86_64/ctrtool /usr/local/bin && \
  rm -rf makerom_ctrtool makerom_ctrtool.zip

WORKDIR /source
CMD ["bash"]
