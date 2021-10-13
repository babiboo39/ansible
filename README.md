# Ansible
This repository is used for learning Ansible

## Environment
- Ansible v2.11.5
- GCP
- Ubuntu 18.04 (bionic)

## Configuration
Before start writing the playbook, we need to define our ansible configuration, which is `ansible.cfg`. This file basically governs the behavior of all interactions on the control node. In this case I use it to configure the `inventory` and other values needed.

## Ansible Inventory
The Ansible inventory file defines the hosts and groups of hosts upon which commands, modules, and tasks in a playbook operate. In this case, I use `inventory.ini` to define the host to be the target of the playbook

## Ansible Roles
Roles let us automatically load vars, tasks, handlers and etc. Roles is used for **reuse** purpose, so let say we have many tasks to do in our playbook, so instead of typing each tasks repeatedly, we can just use roles

To create a new roles, i simply run this command:
```
ansible-galaxy init role init <role-name>
```

*note: to learn more about the ansible, you can read the user guide at* https://docs.ansible.com/ansible/latest/user_guide/index.html

## Usage
Before running this playbook, first change the IP Address of the hosts in the `inventory.ini`, then just run this command
```
ansible-playbook <playbook-name>.yml
```