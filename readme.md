# DinD AlmaLinux/rockylinux Setup

This repository contains Dockerfiles for setting up Docker-in-Docker (DinD) environments using AlmaLinux as the base image. Different configurations are available for various use-cases.

## Table of Contents

1. [Requirements](#requirements)
2. [Installation](#installation)
3. [Dockerfiles Overview](#dockerfiles-overview)
4. [Usage](#usage)
5. [Docker Compose](#docker-compose)
6. [Contributing](#contributing)
7. [Authors](#authors)
8. [License](#license)

## Requirements

- Docker
- Docker Compose (Optional)

## Installation

Clone this repository to your local machine:

```bash
git clone https://github.com/exaluc/DinD.git
```

## Dockerfiles Overview

### Dockerfile

This is the standard setup using AlmaLinux 8. It installs Docker CE, Docker CLI, and Containerd.

### Dockerfile-minimal

This setup uses the minimal AlmaLinux image to provide a lightweight DinD environment. It only installs essential packages to run Docker & docker-compose.

### Dockerfile-py

This setup is optimized for Python development. It includes development tools and Python 3.9.1.

## Usage

To build a Docker image from any of the Dockerfiles, navigate to the project directory and run:

```bash
docker build -f <DockerfileName> -t <your-image-name> .
```

For example, to build an image from `Dockerfile`:

```bash
docker build -f Dockerfile -t my-dind-setup .
```

To run the container:

```bash
docker run --privileged -d --name my-dind-container my-dind-setup
```

## Docker Compose

```bash
docker-compose up -d
```

## Legacy Docker Compose CLI near docker compose

For users who are familiar with older docker-compose, also supported.

## Contributing

If you'd like to contribute, please fork the repository and make changes as you'd like. Pull requests are welcome.

## Authors

- [Lucian](https://github.com/exaluc) - Initial work

## License

MIT

---
