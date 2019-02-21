FROM node:8-alpine

LABEL maintainer="ikigeg <michael@ildesigns.co.uk>"

# Suppress npm info logs that are on by default
ENV NPM_CONFIG_LOGLEVEL=warn

# Create the directory that will contain the app, and make subsequent commands run from this directory
WORKDIR /src

# Install some dependencies for compiling mozjpeg
RUN apk add --no-cache --virtual .build-deps \
    autoconf \
    libtool \
    automake \
    bash \
    g++ \
    make \
    nasm

RUN apk add --no-cache \
    libc6-compat \
    libjpeg-turbo-dev \
    libpng-dev

# Install the known modules that require compiling
RUN npm i image-webpack-loader@3.6.0

# Tidy up our build dependencies
RUN apk del .build-deps
