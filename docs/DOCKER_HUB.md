# Docker Hub

[Docker Hub](https://hub.docker.com/u/whiletruedoio) is the most common way to
store container images. We will also store our images at Docker Hub, so images
are easy to discover and use.

## Reasons

- well known
- easy to use
- good search options
- free for public / open source

## Docs & Links

- Site: <https://hub.docker.com>
- Docs: <https://docs.docker.com>

## Features

- organizations and repositories
- tags, README.md and meta data
- search and ranking options
- auto build
- vulnerability scans (only paid options)

## Usage

There are two major ways to use docker hub.

### Users

User can search and pull images and run the images on a host with a sufficient
container engine installed. For docker the examples are listed below:

```sh
# Search images
$ docker search IMAGE

# Pull image
$ docker pull whiletruedoio/IMAGE[:TAG]

# Run image
$ docker run whiletruedoio/IMAGE[:TAG]
```

### Developers

Developers need to login and push the container to docker. Therefore, it is
recommended to have a Dockerfile that includes important data. Afterwards, one
can either manually or via CI/CD push the new image. At
[while-true-do.io](https://while-true-do.io) we will focus on pushes via CI/CD.
Nevertheless, below steps are for manual development.

```sh
# Build the image
$ docker build -t docker.io/whiletruedoio/IMAGE:TAG .

# Login to docker hub
$ docker login docker.io

# Push image
$ docker push -t docker.io/whiletruedoio/IMAGE:TAG
```

In addition, Docker hub provides options to link a repository and build directly
from new Dockerfiles in a branch.

## Integrations

We want to automatically build and publish new images, based on a branch and
git tag. Additionally, we want to inform developers via Slack, if something new
is published.
