FROM julia-0.6-minimal

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
