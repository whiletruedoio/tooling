# Podman

Podman is a new Docker replacement, which provides a daemonless and rootless
experience. Similar to Docker, you can build, run and publish container
workloads with Podman. Instead of providing a seperate daemon, Podman is
using many systemd mechanisms.

## Reasons

- rootless
- daemonless
- pre-installed/default on most RHEL'ish distributions
- very active development
- can run kubernetes workloads

## Docs & Links

- Site: <https://podman.io>
- Docs: <https://docs.podman.io>
- Code: <https://github.com/containers/podman>

## Features

- rootless and daemonless
- very similar to Docker
- adds SELinux, Firewalld and systemd integrations
- create and run Kubernetes development files
- create systemd services for containers
- ecosystem with buildah and skopeo

## Usage

The usage of Podman is very similar to Docker. At
[while-true-do.io](https://while-true-do.io), we are using it mostly, since it
is the default for Fedora, CentOS and RHEL. In addition it provides additional
features and is a very useful developement software.

### Getting Started

The Podman project provides a handy
[Getting Started Guide](https://podman.io/getting-started/). Be aware, that
some commands are not available in Docker and vice-versa.

### Conventions

Currently, we do not enforce any conventions, but recommend to keep the usage
to a Docker-compatible workflow, for now.
