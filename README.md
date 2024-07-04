# Development Container for Pico SDK

This project is a template that you can use to spin up your own development environment with the [Pico SDK](https://github.com/raspberrypi/pico-sdk) pre-configured, with no need to install anything locally. You will need a GitHub account to use the Codespaces feature.

Currently, you can compile your code and download the resulting elf/uf2 binary files, just as you would with a locally-installed toolchain.

Debugging is currently not supported but can be made to work with some SSH reverse tunneling, a debug probe, and running OpenOCD on the host where your Pico is connected.

## Setting up the development container

### GitHub Codespaces

[Click this link to create a new GitHub Codespace with this template](https://codespaces.new/ndabas/pico-devcontainer-template).

For more info, check out the [documentation](https://docs.github.com/en/codespaces/overview).

### VS Code Dev Containers

If you already have VS Code and Docker installed, you can [click this link to get started](https://vscode.dev/redirect?url=vscode://ms-vscode-remote.remote-containers/cloneInVolume?url=https://github.com/ndabas/pico-devcontainer-template). This will cause VS Code to automatically install the Dev Containers extension if needed, clone the source code into a container volume, and spin up a dev container for use.

More info in the [documentation](https://code.visualstudio.com/docs/devcontainers/containers).
