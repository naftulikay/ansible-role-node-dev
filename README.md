# ansible-role-node-dev [![Build Status][travis.svg]][travis]

Installs and configures a node development environment for a given user using [`nodenv`][nodenv].

Available on Ansible Galaxy at [`naftulikay.node-dev`][galaxy].

## Requirements

Officially tested operating systems are listed in the Galaxy manifest.

## Role Variables

<dl>
  <dt><code>node_user</code></dt>
  <dd>User to install node tools for. Required.</dd>
  <dt><code>node_version</code></dt>
  <dd>Version of node to install. Defaults to 6.11.2.</dd>
<dl>

## Dependencies

None.

## Example Playbook

Here are some example playbooks to get started with.

### Defaults

Simply get a node development environment installed:

```yaml
---
- name: install
  hosts: all
  become: true
  roles:
    - role: node-dev
      node_user: vagrant
```

### Install a Specific Version

Install a specific version of node:

```yaml
---
  - name: install
    hosts: all
    become: true
    roles:
      - role: node-dev
        node_user: vagrant
        node_version: '6.11.2'
```

## License

MIT

 [travis]: https://travis-ci.org/naftulikay/ansible-role-node-dev
 [travis.svg]: https://travis-ci.org/naftulikay/ansible-role-node-dev.svg?branch=master
 [galaxy]: https://galaxy.ansible.com/naftulikay/node-dev/
 [nodenv]: https://github.com/nodenv/nodenv
