FROM ubuntu:18.04

ENV GSNAP_VERSION 2019-03-15
RUN apt-get update \
  && apt-get install --yes make g++ zlib1g-dev libbz2-dev wget perl \
  && cd /tmp \
  && wget http://research-pub.gene.com/gmap/src/gmap-gsnap-${GSNAP_VERSION}.tar.gz \
  && tar xzf gmap-gsnap-$(GSNAP_VERSION}.tar.gz \
  && cd /tmp/gmap-${GSNAP_VERSION} \
  && ./configure --prefix=/usr/local --with-simd-level=sse42 \
  && make \
  && make check \
  && make install \
  && rm -rf /tmp/gmap-* \
  && apt-get remove --purge --yes make g++ wget \
  && apt-get autoremove --purge --yes
