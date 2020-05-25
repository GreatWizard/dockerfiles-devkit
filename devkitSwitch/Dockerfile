# Combination of devkitA64 + devkitARM f.e. to build Atmosphere
FROM greatwizard/devkita64:latest

ENV DEVKITARM $DEVKITPRO/devkitARM
ENV PATH $DEVKITARM/bin:$PATH

RUN wget -nv -O devkitARMupdate.pl https://raw.githubusercontent.com/devkitPro/installer/master/perl/devkitARMupdate.pl && \
	sed -i 's/\/opt\/devkitpro/\/opt\/devkitPro/' devkitARMupdate.pl && \
	perl devkitARMupdate.pl && \
	rm -f devkitARMupdate.pl *.tar.bz2 *.tar.gz *.tar.xz
