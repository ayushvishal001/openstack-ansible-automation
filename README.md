# OpenStack Ansible Automation

This repository contains Ansible playbooks and roles to automate
the deployment and verification of an OpenStack environment.

## Structure
- `inventory/hosts`: Ansible inventory file
- `ansible.cfg`: Ansible configuration
- `playbooks/site.yml`: Main playbook
- `playbooks/roles`: Individual roles (prerequisites, nova, swift, trove)

## Usage
Run the playbook with:
```
ansible-playbook playbooks/site.yml
```

## Notes
- Tested on Ubuntu 22.04 with DevStack.
- Services verified: Nova, Swift, Trove.

