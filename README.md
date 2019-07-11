
# Ansible common/miscellaneous role

This ansible role will uninstall/install defaults Linux packages, and configure services including: hostname, sysctl.conf, and more ...

## Requirements

Ansible >= 2.7

## Usage

Include this role into a playbook

```yaml
- hosts: all
  gather_facts: yes
  become: yes

  roles:
    - { name: "common", tags: ['common'] }
```

