FROM docker:18.06.1-ce

ENV SINGULARITY_VERSION 2.5.2

RUN apk --update add \
  file \
  tar \
  build-base \
  linux-headers \
  libarchive-dev \
  python \
  squashfs-tools \
  bash \
  openssh-client

WORKDIR /tmp
RUN wget https://github.com/sylabs/singularity/releases/download/$SINGULARITY_VERSION/singularity-$SINGULARITY_VERSION.tar.gz \
  && tar xvf singularity-$SINGULARITY_VERSION.tar.gz \
  && cd /tmp/singularity-$SINGULARITY_VERSION \
  && ./configure --prefix=/usr/local \
  && make && make install \
  && cd /tmp \
  && rm /tmp/singularity-$SINGULARITY_VERSION.tar.gz \
  && rm -rf /tmp/singularity-$SINGULARITY_VERSION

RUN apk del \
  build-base \
  linux-headers

CMD ["bash"]

