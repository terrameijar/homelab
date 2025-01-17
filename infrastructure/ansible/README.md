# Ansible playbooks for server provisioning

This playbook contains code to provision a kubenetes server. It upgrades packages and installs kubectl
The `k3s-ansible` directory contains a playbook to set up a k3s cluster.

## Provisioning steps

1. Rename `.env_example` in `infrastructure/ansible/` to `.env`

1. Source the .env file in `infrastructure/ansible/.env` to populate Leader and worker node IPs in the shell.

1. Create the cluster using the playbook in `infrastructure/ansible/k3s-ansible`

1. Run playbooks against the cluster nodes using
   `ansible-playbook setup.yaml`
