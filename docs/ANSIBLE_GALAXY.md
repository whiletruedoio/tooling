# Ansible Galaxy

As you may be aware, we are using [Ansible](./ANSIBLE.md) for some of our work.
[Ansible Galaxy](https://galaxy.ansible.com) is the default library to publish
Ansible roles, collections, plugins and modules. There are options to host the
galaxy software on your own or provide GitHub repositories only - both seems
very unconvenient for users. So, we decided to use the default Ansible Galaxy.

## Reasons

- default library
- no login needed (aside GitHub)
- simple to use
- is maintained by the Ansible community

## Docs & Links

The below list provides some useful links and documentation for Ansible Galaxy.

- Site: <https://galaxy.ansible.com/>
- Docs: <https://galaxy.ansible.com/docs/>

## Features

- supports collections and roles
- ranking and scoring for content
- uploads automatically or manually
- markdown parser for README.md from a repository
- tags, search and links from Ansible meta files
- versioning from GitHub Tags or release versions

## Usage

The general usage of Ansible Galaxy is splitted into users, that download and
use content and developers that publish content.

### Using

Using content from Ansible Galaxy is done with the `ansible-galaxy` command.

You can install a role

```sh
$ ansible-galaxy role install NAMESPACE.ROLENAME
...
- NAMESPACE.ROLENAME (4.7.0) was installed successfully
```

or a collection

```sh
$ ansible-galaxy collection install NAMESPACE.COLLECTION
...
NAMESPACE.COLLECTION:1.0.0 was installed successfully
```

You can learn more about the general usage of Ansible Galaxy in the official
[documentation (cli)](https://docs.ansible.com/ansible/latest/cli/ansible-galaxy.html)
or in this blog [article](https://www.redhat.com/sysadmin/ansible-galaxy-intro).

Each developer of an Ansible repository should provide detailed guides for users.

- [Using Roles](https://docs.ansible.com/ansible/latest/user_guide/playbooks_reuse_roles.html)

### Publish

Publishing new content on Ansible Galaxy is pretty straught forward, too. There
is lots of documentation for
[role](https://galaxy.ansible.com/docs/contributing/creating_role.html)
and
[collection](https://docs.ansible.com/ansible/latest/dev_guide/developing_collections.html)
development available.

You will find detailed development guides in the repository, where the role,
plugin or collection is located.
