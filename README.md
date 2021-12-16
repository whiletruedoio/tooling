<!--
reference: https://www.makeareadme.com/
reference: https://commonmark.org/
-->

# Tooling

Overview and documentation of the tooling used to drive while-true-do.io. Also,
integrations from one service to another. 

## Motivation

As a new contributor, I need an overview and documentation of tools that the
project is using for certain tasks, so I can start working fast.

## Description

This repository describes the different services and tools that are used at
[while-true-do.io](https://while-true-do.io) and are available for all
contributors. If needed, it will also provide snippets, scripts and steps to
reproduce the setup.

### Services

We are consuming several services as SaaS option. This makes it very easy to
setup new stuff and get things going. Creating and maintaining our own
infrastructure is still a thing, but first we want to get stuff done.

#### Ansible Galaxy

[Ansible Galaxy](https://https://galaxy.ansible.com/whiletruedoio) is the
most common way to publish Ansible content like plugins, roles, playbooks and
collections. We also intend to publish our work there.

#### GitHub

[GitHub](https://github.com/whiletruedoio) is our default place to store code,
issues and everything related to coding. This decision was mostly made after
testing a couple of alternatives like [Gitea](https://gitea.com/) and
[GitLab](https://gitlab.com/). GitHub is still the standard to create, maintain
and integrate Open Source projects and provides tons of functionality for free.

You can read more about our reasons and ways to use GitHub
[here](docs/GITHUB.md).

#### LinkedIn

[LinkedIn](linkedin.com/company/whiletruedoio/) is a business network to
interact with companies and experts. It is very common to find tech enthusiasts
on LinkedIn. We are using the platform mostly to send out updates and news or
release announcements.

You can find some details about the integrations and reasons in
[the document](docs/LINKEDIN.md) about LinkedIn.

#### Slack

[Slack](https://whiletruedoio.slack.com) is the internal chat platform, used for
dev-talk and most notifications. This decision was made after testing other
options. Even if Slack is not a perfect solution, it gets things done, that need
more manual work in other chat systems.

You can find more about Slack and how we use it [here](docs/SLACK.md).

#### Twitter

[Twitter](https://twitter.com/whiletruedoio) is a huge social network with lots
of tech enthusiasts. It is easy to access, free and very widely used. At
[while-true-do.io](https://while-true-do.io), we use it mostly to keep users
and contributors informed about new releases, blog articles or updates.

You can find all the details and integrations in [this](docs/TWITTER.md)
document.

#### UptimeRobot

[UptimeRobot](https://stats.uptimerobot.com/zKXjluyAr/) provides a very easy
and convenient way to monitor infrastructure, web services and more. You are
also able to provide a statuspage and alert integrations. The free plan allows
us to monitor our services and get alerts in our preferred ways.

You can learn more about the usage and reasons at
[while-true-do.io](https://while-true-do.io) in the
[documentation](docs/UPTIMEROBOT.md).

#### Zapier

[Zapier](https://zapier.com) is the glue between the used services. If a
service does not provide integrations in another service, we can most often
use webhooks or other functionality via Zapier.

You can find a list of these integrations and the reasons behind the decision
in [this](docs/ZAPIER.md) document.

## Software

At [while-true-do.io](https://while-true-do.io), we agreed to use some software
and ensure it is working as desired. Nobody is forced to use the same stack,
but if you need some help from the community, it is recommended to check the
default software.

### Ansible

For automation purposes, we use [Ansible](https://www.ansible.com) most of the
time. Since Ansible provides options for setup and operations, it was chosen. It
is also easy to learn and provides thousands of integrations.

If you intend to use Ansible or maintain Ansible Code, it is highly recommended
to read our [Ansible Documentation](docs/ANSIBLE.md) beforehand.

### k3s/k3os

Using Kubernetes was somewhat mandatory to ensure that we can maintain our
software in a declaritive and consistent way. After lots of investigation,
we made the decision to use k3s/k3os as our base and focus on a Kubernetes-only
workflow.

You can read more about [k3s](https://k3s.io/) and [k3os](https://k3os.io/)
beforehand and also check our own [documentation](docs/K3OS.md).

### Kubernetes

On top of k3s, we are doing Kubernetes deployments and deploy containers. This
was the most convenient way to establish a proper lifecycle management and
ensure that nothing is changed by accident.

You can read more about the reasons and guidelines in the Kubernetes
[document](docs/KUBERNETES.md).

### Support

We are making the software in our freetime and without payment. Nevertheless,
we try to support you wherever possible. In case you want to get in touch with
us, please have a look at the [Contact](#Contact) options and the
[Support Guide](docs/SUPPORT.md).

## Contribute

Thank you so much for considering to contribute! We are happy, when someone is
joining the hard work. Please have a look at the
[Contributor Conventions](https://github.com/whiletruedoio/.github/blob/main/docs/CODE_OF_CONDUCT.md)
beforehand.

### Issues

Issues and Pull Requests are handled on a regular basis. Please be aware, that
we may reach out to you, ask you to provide additional resources or want to
discuss the issue a little, before planning it.

- [Bugs and Feature Requests](https://github.com/whiletruedoio/tooling/issues)
- [Pull Requests](https://github.com/whiletruedoio/tooling/pulls)

### Develop

Providing code to this repository is pretty straight forward. Open an issue,
so we can discuss the bug/feature and start working on it afterwards. You just
need to open the pull request afterwards and that's it.

It is also strongly recommended to read the
[Contribution Guideline](https://github.com/whiletruedoio/.github/blob/main/docs/CONTRIBUTING.md)
beforehand.

### Changelog

We are maintaining a [changelog](CHANGELOG.md) for repositories. Normally, the
developers will update the changelog, according to
[keepachangelog.com](https://keepachangelog.com/).

## License

Except otherwise noted, all work is [licensed](LICENSE) under a
[BSD-3-Clause License](https://opensource.org/licenses/BSD-3-Clause).

## Contact

Please feel free to reach out to us and the community. We also recommend to read
and understand the
[Code of Conduct](https://github.com/whiletruedoio/.github/blob/main/docs/CODE_OF_CONDUCT.md)
beforehand.

- Site: <https://while-true-do.io>
- Blog: <https://blog.while-true-do.io>
- Code: <https://github.com/whiletruedoio>
- Chat: [libera.chat #whiletruedoio](https://web.libera.chat/gamja/#whiletruedo)
- Mail: [hello@while-true-do.io](mailto:hello@while-true-do.io)
