
# Ansible common role

This ansible role will uninstall/install defaults Linux packages, and configure services including: hostname, sysctl.conf, and more ...

## Requirements

Ansible >= 2.7

## Usage

Include this role into a playbook

```yaml
---
- hosts: wireguard_master
  gather_facts: yes
  become: true
  vars:
    ansible_ssh_user             : "ubuntu"
    ansible_ssh_private_key_file : "~/.ssh/nfq-tools"
    ansible_python_interpreter   : "/usr/bin/python3"
    project_name  : "nfq"
    env           : "tools"
  roles:
    - role: nfq.common
      vars:
        vm_hostname: "{{ project_name }}-{{ env }}-wireguard"
```

