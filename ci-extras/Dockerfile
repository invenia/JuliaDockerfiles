ARG JULIA_TAG=latest
FROM invenia/julia:$JULIA_TAG

MAINTAINER Invenia Technical Computing

LABEL julia_install=extras

# useful packages for building dependencies
RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y \
		hdf5-tools \
		git \
		unzip \
		build-essential

RUN julia -e "Pkg.add(\"Coverage\"); using Coverage"
