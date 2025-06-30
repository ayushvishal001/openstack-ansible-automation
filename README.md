# OpenStack Deployment Automation with Ansible

This repository contains an Ansible-based automation setup to validate an OpenStack DevStack deployment and check the status of core services like Nova, Swift, and Trove.

---

## 📁 Directory Structure


---

## 🚀 How to Run

Make sure your DevStack environment is already running and DevStack services are active (e.g., `nova-api`, `swift-proxy`, `trove-api`).

Then execute:

```bash
ansible-playbook playbooks/site.yml

TASK [nova : Check if nova-api service is running]
changed: [localhost]

TASK [nova : Print Nova API service status]
ok: [localhost] => {
    "msg": "nova-api service is active"
}

TASK [swift : Check if swift-proxy service is running]
fatal: [localhost]: FAILED! => {"stdout": "inactive"}
...ignoring

TASK [swift : Print Swift proxy service status]
ok: [localhost] => {
    "msg": "swift-proxy service is inactive"
}



---

Once you paste this into `README.md`, save and commit it like this:

```bash
git add README.md
git commit -m "Add complete README with structure, usage, and sample output"

