# Git

[Git](https://git-scm.com/) is the most commonly used source code management for
Open Source projects (and maybe all development projects). It is also required
by [GitHub](./GITHUB.md) and we are using it at
[while-true-do.io](https://while-true-do.io) for our source code repositories.

## Reasons

- very powerful SCM
- very widely used
- known by many developers
- default for GitHub
- well documented

## Docs & Links

- Site: <https://git-scm.com/>
- Docs: <https://git-scm.com/doc>
- Code: <https://github.com/git/git>

## Features

- decentralized SCM
- small footprint
- fast
- easy to learn
- multiple workflows

## Usage

At [while-true-do.io](https://while-true-do.io), we use Git and Git workflows
for almost all of our work. Therefore, we want to provide a little guidance for
the usage of Git.

### Getting Started

To get started with Git, you need to [install](https://git-scm.com/downloads)
Git on your machine. Git is available for different operating systems: please
choose the one you are using. It is not recommended to start with a graphical
interface, if you just start using Git, but to stick with the command line for
a while. Nevertheless, there are hundreds of integrations and desktop clients
available.

After the installation, you can check out the
[beginner guides](https://git-scm.com/doc) in the official documentation and
have a look at the
[GitHub Docs](https://docs.github.com/en/get-started/getting-started-with-git),
which also provide some lessons about Git itself.

### Meta files

We do have some meta files included in our repositories. These are not meant to
be read by Humans, but will be used from software. For Git, we do have at least
the below listed files.

- [.gitignore](https://git-scm.com/docs/gitignore)
- [.gitattributes](https://git-scm.com/docs/gitattributes)
- [.gitmessage](https://git-scm.com/book/en/v2/Customizing-Git-Git-Configuration)

We strongly encourage you to get an idea how they work and what they do.

### Workflow

The [while-true-do.io](https://while-true-do.io) workflow for contributions is
really easy. We have a small summary of the below in our
[Contribution Guideline](https://github.com/whiletruedoio/.github/blob/main/docs/CONTRIBUTING.md).

In general, we are working in a
[trunk based workflow](https://trunkbaseddevelopment.com/). This means, that
each and every feature, fix or general update will be branched from and merged
to the "main" branch. Grahically, this will look something like this:

```ascii

[main] [abc123] --------> [def456] -> [ghi789]
           |-> [feature a] ->|            |
           |-> [feature b] -------------->|
```

This makes it very easy to seperate features and fixes from each other and
review them. On the other hand, it introduces the need to fix conflicts on
the developer side. This can be done with a "rebase" from the developer, before
opening a pull request.

The workflow is the very same if you are forking or directly working on a
branch and boils down to:

1. Create or assign the issue
2. Create a fork or a branch (in best case named similar to the issue
   "enhancement/Git_workflow" or "bug/broken_links)
3. Develop you code
4. Commit your contribution
5. Rebase your code to integrate updates from "main" and maybe "squash" your
   commits
6. Open a Pull request
7. Follow up in the review process

Depening on the repository, you need to run tests or request a review, but in
general that is is.

### Conventions

We don't want to make it too complicated to contribute and therefore the
conventions are not written in stone. Nevertheless, you should check, if you
can:

- always assign or open an issue before starting to work
- sign your commits with a proper gpg key
- use a proper commit message as described in the [.gitmessage](../.gitmessage)
- follow the [Contribution Guideline](https://github.com/whiletruedoio/.github/blob/main/docs/CONTRIBUTING.md)
