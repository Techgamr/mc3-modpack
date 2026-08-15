FROM mcr.microsoft.com/devcontainers/base:ubuntu

# Install Go and git so packwiz can be installed during image build.
RUN apt-get update \
    && apt-get install -y --no-install-recommends golang-go git ca-certificates

ENV GOPATH=/usr/local/go
ENV PATH=${GOPATH}/bin:${PATH}

# Install packwiz during build so it is available immediately when the container opens.
RUN go install github.com/packwiz/packwiz@latest
