
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

## Fully upgrade Linux distribution

When fully upgrade OS is required, add this variable in your playbook's vars block:

```yaml
    vars:
      upgrade_os_enabled: true
```

It will run `apt dist-upgrade -y` then reboot server(s) afterwards.
