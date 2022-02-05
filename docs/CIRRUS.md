# Cirrus CI / Cirrus CLI

At [while-true-do.io](https://while-true-do.io), we want to automate a lot to
reduce manual effort and establish a high quality of code. We opted for Cirrus,
since it provides a nice integration in [GitHub](GITHUB.md), a Command Line
Interface and a cloud service, that can be used for free.

## Reasons

Opting for one solution that really works for our demand was not an easy task.
In fact, there are hundreds of services available and even [GitHub](GITHUB.md)
provides its own service (GitHub Actions). Here are some reasons, why it became
Cirrus CI in the end.

- has a client for local testing (Cirrus CLI)
- works with Docker and Podman
- free for public/Open Source repositories
- easy to understand container tasks

## Docs & Links

- Site: <https://cirrus-ci.org/>
- Docs: <https://cirrus-ci.org/guide/quick-start/>
- Blog: <https://medium.com/cirruslabs>

## Features

- free for Open Source/public GitHub repositories
- works in containers of your choice
- integrations in many services
- credential handling
- simple task definitions in YAML

## Usage

When it comes to usage, you may want to have an additional read in the official
documentation. This little section will give a very brief introduction of our
usage at [while-true-do.io](https://while-true-do.io).

### Cirrus CI

We use Cirrus CI for all kind of tasks, that need automation. You can have a
look in the [template repository](https://github.com/whiletruedoio/template/)
for a very simple pipeline.

All repositories in the [GitHub organization](https://github.com/whiletruedoio)
can use Cirrus CI out of the box. You just need to add the proper configuration
file (a .cirrus.yml) to the repository and push your changes.

Cirrus CI works with containers only. That means, if you want to execute a task
it will be running in a container. The container image must be defined
beforehand and dependencies must be installed by your pipeline.

It is strongly recommended to check if your repository contains some tests,
fitting to your code. A small list of testing scenarios is below.

Please also check out the
[Cirrus CI documentation](https://cirrus-ci.org/guide/quick-start/), which
contains examples for several use cases.

### Cirrus CLI

Cirrus CLI is a command line client to run your Cirrus CI Pipeline locally.
This allows you to test a pipeline before pushing it. You need to download
[Cirrus CLI](https://github.com/cirruslabs/cirrus-cli) beforehand. Furthermore,
you will need Podman or Docker installed on your machine.

Using Cirrus CLI locally boils down to:

```sh
$ cirrus run
✅ 'Lint Markdown' Task 8.3s
✅ 'Lint YAML' Task 9.3s
```

It is strongly recommended to use Cirrus CLI locally before opening a pull
request and also add more steps to the pipeline, if your contribution demands
it.

In case you are using Podman as the backend, you need to install
"podman-docker", too. Otherwise Cirrus CLI will fail, when it comes to
`docker_builder` tasks.

### Testing Scenarios

Testing can mean everything and nothing. There are hundreds of tests possible
for different code and levels of testing. In general, we are sticking to the
below list and encourage you to use the tests, if they are helpful for
development or provide security or quality to the code.

- sanity checks: basically code quality checkers, static code analyzers or
  linters
- functional tests: a superset of different tests, that test for
  functionality of a feature or code
  - unit tests: meant to test a single module or function of your code
  - integration tests: should test if modules work together and are reliable
- security testing: is a superset of different tests, that target to improve
  the security of your code and can be done in different categories
  - Confidentiality
  - Integrity
  - Authentication
  - Availability

Please consider to add tests to your code or the pipeline to keep the quality
of your code high. Please also keep in mind, that there is no "100% tested"
scenario, but that shipped bugs indicate that our testing is not good enough.

## Integration

All repositories in our [GitHub Organization](https://github.com/whiletruedoio)
can tested by adding a "cirrus.yml" file. Afterwards, the tests will run
automatically, as configured. You will also see the test status in GitHub at
several places like the repository overview, [shields](SHIELDS.md) or in pull
requests.

Additional integrations to [Slack](SLACK.md) are not used, yet.

## Bot Users

There are situations, where you need to have a technical user / bot user, that
can access certain resources (ex.: pushing a container to Docker Hub via CI/CD).

These users can be requested from the
[maintainers](https://github.com/whiletruedoio/organization/blob/main/docs/PEOPLE.md#maintainers)
and will given to you as an encrypted value. This calue can be decrypted from
the Cirrus CI.

In case such an encrypted value becomes vulnerable or invalid, please reach out
to the maintainers immediately, so we can revoke and re-create the users.
