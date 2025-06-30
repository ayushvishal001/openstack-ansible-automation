# OpenStack Automated Deployment using Ansible

This project automates the deployment and validation of an OpenStack environment on a single-node setup using Ansible.

## Overview
- OpenStack is deployed with DevStack on Ubuntu 22.04.
- Services included:
  - Nova (compute)
  - Neutron (network)
  - Keystone (identity)
  - Swift (object storage)
- Trove (database service) was intentionally skipped to keep the setup stable.

## Inventory
All OpenStack components run on a single node managed via Ansible.

Example hosts.ini:

[openstack_nodes]
localhost ansible_connection=local





## Running Ansible Playbooks
Use these playbooks to verify the environment.

### Check OpenStack services and Swift
ansible-playbook -i hosts.ini check_openstack.yml



### Check high availability status of key services
ansible-playbook -i hosts.ini ha_check.yml


These ensure that important services are running and Swift is responding correctly.

## Notes
- This setup is designed for a local development or test environment.
- The HA checks verify that critical systemd services for Nova, Neutron, and Swift are active.



#We can  add Trove, we can do it cleanly by:

Adding enable_service trove tr-api tr-tmgr tr-cond in local.conf.

Running stack.sh again.

Writing a minimal Ansible check for devstack@tr-* services.
