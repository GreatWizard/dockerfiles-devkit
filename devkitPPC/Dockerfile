FROM debian:stretch
MAINTAINER Guillaume Gérard "guillaume.gerard88@gmail.com"

# These dictate where to install devkitPro/PPC and dictate where they are found
# in project makefiles.
ENV DEVKITPRO /opt/devkitPro
ENV DEVKITPPC $DEVKITPRO/devkitPPC

RUN apt-get update && \
  apt-get install -y \
    bzip2 \
    make \
    perl \
    wget && \
  rm -rf /var/lib/apt/lists/*

ADD https://raw.githubusercontent.com/devkitPro/installer/master/perl/devkitPPCupdate.pl devkitPPCupdate.pl
RUN perl devkitPPCupdate.pl && \
  rm /devkitPPCupdate.pl /*.tar.bz2

RUN mkdir /source
WORKDIR /source
CMD ["bash"]
