FROM debian:buster-slim
LABEL maintainer="Akira Koyasu <mail@akirakoyasu.net>"

# sample:
#
# docker run --rm -it \
#   -v ${PWD}:/cafeobj \
#   akirakoyasu/cafeobj \
#   -batch sample.cafe
#

ARG VERSION=1.6.0
ARG LISP=acl

ADD https://cafeobj.org/files/${VERSION}/cafeobj-${VERSION}-${LISP}-x64Linux.tar.gz /usr/local/src/
RUN cd /usr/local/ && tar xvfz /usr/local/src/cafeobj-${VERSION}-${LISP}-x64Linux.tar.gz

ENTRYPOINT ["cafeobj"]
VOLUME /cafeobj
WORKDIR /cafeobj
