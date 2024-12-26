# Use a lightweight Debian image as the base
FROM debian:bullseye-slim

# Set environment variables to avoid interactive prompts during package installation
ENV DEBIAN_FRONTEND=noninteractive

# Install required C development packages
RUN apt-get update && apt-get install -y \
    build-essential \
    gcc \
    g++ \
    make \
    cmake \
    gdb \
    clang \
    valgrind \
    git \
    curl \
    && rm -rf /var/lib/apt/lists/*

# Set the working directory inside the container
WORKDIR /workspace

# Clean up apt cache to reduce image size
RUN apt-get clean

# Default command to run
CMD [ "bash" ]
