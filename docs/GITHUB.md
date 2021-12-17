# GitHub

After evaluating source code management software over the last years and testing
basically every huge provider and also self-host some software, we cam to the
conclusion to go back to GitHub. This document describes why we are now on
GitHub and which features we use.

## Reasons

Below you can find some reasons why we decided to use GitHub.

- other services do provide login-with-github
- very widely used
- free for Open Source projects, including Actions, Wiki and more
- tons of useful features like issues, wiki, CI/CD, package hosting
- there are thousands of integrations in IDEs and services available
- you will have a GitHub account anyway, if you contribute to other Open Source
  projects
- k3os and Ansible Galaxy rely on GitHub or can use it to add features
- you can use static pages, containers and packages on GitHub

## Features

At [while-true-do.io](https://while-true-do.io), we use some features directly
in GitHub.

### general features

Most SCM solutions do provide a list of features, that we also use. The below
list gives an overview of the project/organisation wide used features.

- [ ] emoji
- [x] issues
- [x] labels
- [x] markdown parser
- [x] package registry
- [x] permission management
- [ ] projects
- [x] pull requests
- [x] reviewes
- [ ] wiki

### github repository

We use a [.github repository](https://github.com/whiletruedoio/.github) to
provide default documents and issue templates for all repositories. We also have
a profile document, that welcomes new users and contributors.

- [Reference](https://docs.github.com/en/communities/setting-up-your-project-for-healthy-contributions/creating-a-default-community-health-file)

### issue templates

Issue templates are maintained in the
[.github repository](https://github.com/whiletruedoio/.github)
and are available in all repositories. This makes it very easy and convenient
to have proper formated issues and provide additional links and questions.

- [Reference](https://docs.github.com/en/communities/using-templates-to-encourage-useful-issues-and-pull-requests)

### template repository

We use a [template repository](https://github.com/whiletruedoio/template) to
provide a skeleton for new repositories. This makes it very easy to create a new
repository and include some standard files.

- [Reference](https://docs.github.com/en/repositories/creating-and-managing-repositories/creating-a-template-repository)

## Usage

Using GitHub is quite easy, but if you are completely new to Git/GitHub, you may
need some guidance. After the registration, you can check out the below options.

### GitHub applications

GitHub offers Desktop and Mobile applications to manage your projects and issues.
This is very convenient, since you don't need a browser and will be informed via
push-notifications.

You can also manage issues, pull requests and much more in the applications.

- <https://desktop.github.com/>
- <https://github.com/mobile/>

### git client

For many developers, using Git means using the command line. You can use GitHub
with a regular Git client.

- <https://git-scm.com/>

## Integrations

There are hundreds of integration options for GitHub. There are some widely
accepted and used integrations in our community that are explained in the proper
documents as listed below.

- [Slack](./SLACK.md)
- [VSCode](./VSCODE.md)
