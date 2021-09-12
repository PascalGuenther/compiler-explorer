# See here for image contents: https://github.com/microsoft/vscode-dev-containers/tree/v0.194.0/containers/cpp/.devcontainer/base.Dockerfile

# [Choice] Debian / Ubuntu version: debian-11, debian-10, debian-9, ubuntu-20.04, ubuntu-18.04
ARG VARIANT="buster"
FROM mcr.microsoft.com/vscode/devcontainers/cpp:0-${VARIANT}

# [Optional] Uncomment this section to install additional packages.
RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends \
    build-essential libc6-dev-i386 \
    gcc-8 g++-8 \
    gcc-9 g++-9 \
    gcc-10 g++-10 \
    clang-8 \
    clang-9 \
    clang-10 \
    gcc-arm-none-eabi

RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y install --no-install-recommends npm

RUN curl -sL https://deb.nodesource.com/setup_12.x | bash - && sudo apt -y install nodejs

# RUN wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.3/install.sh | bash \
#    &&  export NVM_DIR="$HOME/.nvm" && [ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh" && [ -s "$NVM_DIR/bash_completion" ] && \. "$NVM_DIR/bash_completion" \
#    &&  nvm install 12