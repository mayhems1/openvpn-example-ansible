# OpenVPN Server at a VPS

Ansible roles and playbooks for OpenVPN Server at a VPS - example

## Requirements

* VPS with Linux Debian based distr
* SSH access
* sudo / root access

## Roles

* roles/openvpn-server - Install and basic configuration of OpenVPN Server

## How to use

define IP address of VPS at inventory/group_vars/all.yml

start playbook

```bash
ansible-playbook -i inventory/hosts server.yml -bKk
```

## To do

* add tasks to configure iptables
* add tasks to configure nat
