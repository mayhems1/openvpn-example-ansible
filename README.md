# OpenVPN Server at a VPS

Ansible roles and playbooks for OpenVPN Server at a VPS - example

## Requirements

* VPS with Linux Ubuntu 20.04 distr
* SSH access
* sudo / root access

## Roles

* roles/openvpn-server - Install and basic configuration of OpenVPN Server

## How to use

define IP address of VPS at inventory/hosts

start playbook

```bash
ansible-playbook -i inventory/hosts server.yml -bKk

# with user

ansible-playbook -i inventory/hosts server.yml -bKk -u root
```

## To do

* add tasks to configure iptables
* add tasks to configure nat
