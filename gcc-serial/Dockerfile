FROM docker.io/ubuntu:latest

LABEL maintainer="lbertag@sandia.gov"

ENV DEBIAN_FRONTEND=noninteractive

# Install basic utils
RUN apt-get update &&   \
    apt-get install -y  \
        curl            \
        git             \
        cmake           \
        locate          \
        vim             \
        wget

# Install compilers
RUN apt-get update &&   \
    apt-get install -y  \
        build-essential \
        gcc             \
        g++             \
        gfortran

# Install MPI
RUN apt-get update &&   \
    apt-get install -y  \
        libopenmpi-dev

# Install blas, yaml-cpp, boost
RUN apt-get update &&   \
    apt-get install -y  \
        libyaml-cpp-dev \
        libboost-dev    \
        libopenblas-dev

# Install hdf5, netcdf, pnetcdf, metis, parmetis
RUN apt-get update &&       \
    apt-get install -y      \
        libhdf5-openmpi-dev \
        libnetcdf-mpi-dev   \
        libpnetcdf-dev      \
        libmetis-dev        \
        libparmetis-dev

CMD [ "/bin/bash" ]
