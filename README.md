# Ansible role [zabbix_proxy](https://galaxy.ansible.com/ui/standalone/roles/buluma/zabbix_proxy/documentation)

Install and configure zabbix-proxy on your system.

|GitHub|Version|Issues|Pull Requests|Downloads|
|------|-------|------|-------------|---------|
|[![github](https://github.com/buluma/ansible-role-zabbix_proxy/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-zabbix_proxy/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-zabbix_proxy.svg)](https://github.com/buluma/ansible-role-zabbix_proxy/releases/)|[![Issues](https://img.shields.io/github/issues/buluma/ansible-role-zabbix_proxy.svg)](https://github.com/buluma/ansible-role-zabbix_proxy/issues/)|[![PullRequests](https://img.shields.io/github/issues-pr-closed-raw/buluma/ansible-role-zabbix_proxy.svg)](https://github.com/buluma/ansible-role-zabbix_proxy/pulls/)|[![Ansible Role](https://img.shields.io/ansible/role/d/buluma/zabbix_proxy)](https://galaxy.ansible.com/ui/standalone/roles/buluma/zabbix_proxy/documentation)|

## [Example Playbook](#example-playbook)

This example is taken from [`molecule/default/converge.yml`](https://github.com/buluma/ansible-role-zabbix_proxy/blob/master/molecule/default/converge.yml) and is tested on each push, pull request and release.

```yaml
---
- name: Converge
  hosts: all
  become: true
  gather_facts: true

  roles:
    - role: buluma.zabbix_proxy
```

The machine needs to be prepared. In CI this is done using [`molecule/default/prepare.yml`](https://github.com/buluma/ansible-role-zabbix_proxy/blob/master/molecule/default/prepare.yml):

```yaml
---
- name: Prepare
  hosts: all
  gather_facts: false
  become: true

  roles:
    - role: buluma.bootstrap
    - role: buluma.ca_certificates
    - role: buluma.zabbix_repository
```

Also see a [full explanation and example](https://buluma.github.io/how-to-use-these-roles.html) on how to use these roles.

## [Role Variables](#role-variables)

The default values for the variables are set in [`defaults/main.yml`](https://github.com/buluma/ansible-role-zabbix_proxy/blob/master/defaults/main.yml):

```yaml
---
# defaults file for zabbix_proxy

# The mode to operate in, 0 is active, 1 is passive.
zabbix_proxy_mode: "0"

zabbix_proxy_server: "127.0.0.1"

zabbix_proxy_server_port: 10051

zabbix_proxy_hostname: "{{ ansible_fqdn }}"

zabbix_proxy_database_hostname: localhost
zabbix_proxy_database_name: zabbix_proxy
zabbix_proxy_database_user: zabbix
zabbix_proxy_database_password: zabbix
zabbix_proxy_database_port: 3306
```

## [Requirements](#requirements)

- pip packages listed in [requirements.txt](https://github.com/buluma/ansible-role-zabbix_proxy/blob/master/requirements.txt).

## [State of used roles](#state-of-used-roles)

The following roles are used to prepare a system. You can prepare your system in another way.

| Requirement | GitHub | Version |
|-------------|--------|--------|
|[buluma.bootstrap](https://galaxy.ansible.com/buluma/bootstrap)|[![Ansible Molecule](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-bootstrap/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-bootstrap.svg)](https://github.com/shadowwalker/ansible-role-bootstrap)|
|[buluma.ca_certificates](https://galaxy.ansible.com/buluma/ca_certificates)|[![Ansible Molecule](https://github.com/buluma/ansible-role-ca_certificates/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-ca_certificates/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-ca_certificates.svg)](https://github.com/shadowwalker/ansible-role-ca_certificates)|
|[buluma.zabbix_repository](https://galaxy.ansible.com/buluma/zabbix_repository)|[![Ansible Molecule](https://github.com/buluma/ansible-role-zabbix_repository/actions/workflows/molecule.yml/badge.svg)](https://github.com/buluma/ansible-role-zabbix_repository/actions/workflows/molecule.yml)|[![Version](https://img.shields.io/github/release/buluma/ansible-role-zabbix_repository.svg)](https://github.com/shadowwalker/ansible-role-zabbix_repository)|

## [Context](#context)

This role is a part of many compatible roles. Have a look at [the documentation of these roles](https://buluma.github.io/) for further information.

Here is an overview of related roles:

![dependencies](https://raw.githubusercontent.com/buluma/ansible-role-zabbix_proxy/png/requirements.png "Dependencies")

## [Compatibility](#compatibility)

This role has been tested on these [container images](https://hub.docker.com/u/buluma):

|container|tags|
|---------|----|
|[EL](https://hub.docker.com/r/buluma/enterpriselinux)|8|
|[Debian](https://hub.docker.com/r/buluma/debian)|bullseye|
|[opensuse](https://hub.docker.com/r/buluma/opensuse)|all|
|[Ubuntu](https://hub.docker.com/r/buluma/ubuntu)|focal, bionic, noble, jammy|

The minimum version of Ansible required is 2.12, tests have been done to:

- The previous version.
- The current version.
- The development version.

If you find issues, please register them in [GitHub](https://github.com/buluma/ansible-role-zabbix_proxy/issues)

## [Changelog](#changelog)

[Role History](https://github.com/buluma/ansible-role-zabbix_proxy/blob/master/CHANGELOG.md)

## [License](#license)

[Apache-2.0](https://github.com/buluma/ansible-role-zabbix_proxy/blob/master/LICENSE)

## [Author Information](#author-information)

[Shadow Walker](https://buluma.github.io/)
