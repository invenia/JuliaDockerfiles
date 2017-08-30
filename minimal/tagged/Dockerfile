FROM ubuntu:16.04

MAINTAINER Invenia Technical Computing

ARG JULIA_VERSION
ENV JULIA_VERSION $JULIA_VERSION

ARG JULIA_PATCH
ENV JULIA_PATCH ${JULIA_PATCH:--latest}

ENV JULIA_BIN_HOST "https://julialang-s3.julialang.org"
ENV JULIA_URL "$JULIA_BIN_HOST/bin/linux/x64/$JULIA_VERSION/julia-${JULIA_VERSION}${JULIA_PATCH}-linux-x86_64.tar.gz"
ENV JULIA_ROOT /usr/local

LABEL julia_version=$JULIA_VERSION$JULIA_PATCH
LABEL julia_install=minimal

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y \
		curl

RUN curl -s -L --retry 7 $JULIA_URL | tar -C $JULIA_ROOT --strip-components=1 -xzf -
