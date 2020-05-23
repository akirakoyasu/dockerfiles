FROM debian:jessie-slim
LABEL maintainer="Akira Koyasu <mail@akirakoyasu.net>"

# sample:
#
# docker run --rm -it \
#   -v ${PWD}:/cafeobj \
#   akirakoyasu/cafeobj \
#   -batch sample.cafe
#

ARG VERSION=1.5.7

ADD https://cafeobj.org/files/${VERSION}/cafeobj-${VERSION}-sbcl-x64Linux.tar.gz /usr/local/src/
RUN cd /usr/local/ && tar xvfz /usr/local/src/cafeobj-${VERSION}-sbcl-x64Linux.tar.gz

ENTRYPOINT ["cafeobj"]
VOLUME /cafeobj
WORKDIR /cafeobj
