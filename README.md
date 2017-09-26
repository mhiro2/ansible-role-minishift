Ansible Role: minishift
=======================

[![MIT License](https://img.shields.io/badge/License-MIT-blue.svg?style=flat)](https://github.com/mhiro2/ansible-role-minishift/blob/master/LICENSE.txt)
[![Build Status](https://travis-ci.org/mhiro2/ansible-role-minishift.svg?branch=master)](https://travis-ci.org/mhiro2/ansible-role-minishift)

Install [minishift](https://github.com/minishift/minishift) and dependencies.

Requirements
------------

- Target: CentOS 7.x
- Ansible version: 2.4 or later

Role Variables
-----------------

### Default role variables

```
minishift_version: '1.6.0'
minishift_repo_url: "https://github.com/minishift/minishift/releases/download/v{{ minishift_version }}/minishift-{{ minishift_version }}-linux-amd64.tgz"
minishift_checksum: sha256:b646a9d30eca19b21ca42ff190cd4f4d14d5944ec4ad49145ff989a78bba9ec5

minishift_install_path: /usr/local/bin

kvm_driver_version: 0.7.0
kvm_driver_repo_url: "https://github.com/dhiltgen/docker-machine-kvm/releases/download/v{{ kvm_driver_version }}/docker-machine-driver-kvm"
kvm_driver_checksum: sha256:c4ff3eeb5b232aad41942feb8fb46aaaf8d54239408e2f6549468c997a845a31
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: mhiro2.minishift, tags: ['minishift'] }

License
-------

MIT

Author Information
------------------

[Masaaki Hirotsu](<mailto:hirotsu.masaaki@gmail.com>)

