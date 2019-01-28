
# Ansible common/miscellaneous role

This ansible role will fully upgrade Linux distribution, uninstall/install defaults Linux packages, and configure services including: sysctl.conf, NTP, and more ...

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

## Attention!

This role will upgrade Linux distribution to the latest version then reboot instance(s) afterwards. So use this role with cautious.