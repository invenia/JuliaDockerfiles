FROM ubuntu:16.04

MAINTAINER Invenia Technical Computing

ENV JULIA_VERSION latest

ENV JULIA_BIN_HOST "https://julialangnightlies-s3.julialang.org"
ENV JULIA_URL "$JULIA_BIN_HOST/bin/linux/x64/julia-latest-linux64.tar.gz"
ENV JULIA_ROOT /usr/local

LABEL julia_version=latest
LABEL julia_install=minimal

RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y \
		curl

RUN curl -s -L --retry 7 $JULIA_URL | tar -C $JULIA_ROOT --strip-components=1 -xzf -
