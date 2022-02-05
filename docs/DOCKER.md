# Docker

Docker is the most known container software and also very well established in
the tech industries. This document will cover the software (namely Docker CLI
and Docker daemon) and why we are using it.

For Docker Hub (the central Docker Marketplace / Image registry), please check
out the [Docker Hub Document](./DOCKER_HUB.md).

## Reasons

- very well known
- works on Windows, MacOS, Linux
- good support
- lots of integrations available
- free

## Docs & Links

- Site: <https://docker.com>
- Docs: <https://docs.docker.com>
- Code: <https://github.com/moby/moby>

## Features

- pull, build and publish container images
- run, maintain, manage containers
- can be used for development and operations

## Usage

The usage of Docker in [while-true-do.io](https://while-true-do.io) is mostly
on developer workstations and in [Cirrus CI](./CIRRUS.md) pipelines. We are
using it for testing, building and publishing images.

### Getting Started

To get started, we strongly recommend having a look at the official
[Getting Started Guide](https://www.docker.com/get-started), which covers all
basic use cases. For writing Dockerfiles, you should also have a look at the
[Dockerfile reference](https://docs.docker.com/engine/reference/builder/).

In addition, we have also published a couple of articles about Docker and
Podman in the [blog](https://blog.while-true-do.io/tags/container/).

### Conventions

We try to lead the conventions by example for now. You can find some
guidance and documentation in the
[container-template repository](https://github.com/whiletruedoio/container-template).
