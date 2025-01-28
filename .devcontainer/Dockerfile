FROM ubuntu:latest
# https://octopus.com/blog/using-ubuntu-docker-image
RUN echo 'APT::Install-Suggests "0";' >> /etc/apt/apt.conf.d/00-docker
RUN echo 'APT::Install-Recommends "0";' >> /etc/apt/apt.conf.d/00-docker
RUN DEBIAN_FRONTEND=noninteractive \
  apt-get update \
  && apt-get install -y python3 \
  && apt-get install -y git \
  && apt-get install -y rsync \
  && apt-get install -y ssh \
  && apt-get install -y mercurial \
  && apt-get install -y bubblewrap \
  && apt-get install -y opam=2.3.0 \
  && rm -rf /var/lib/apt/lists/*

# Running as root to make dev easy.
#RUN useradd -ms /bin/bash opam
#USER opam
