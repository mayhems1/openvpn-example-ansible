# OpenVPN Server at a VPS

Ansible roles and playbooks for OpenVPN Server at a VPS - example

## Requirements

* VPS with Linux Debian based distr
* SSH access
* sudo / root access

## Roles

* roles/openvpn-server - Install and basic configuration of OpenVPN Server
* roles/iptables - configuration iptables

## How to use

define IP address of VPS at inventory/group_vars/all.yml

start playbook

```bash
ansible-playbook -i inventory/hosts server.yml -bKk
```

## Example playbook

```yaml
- name: openvpn-server
  hosts: vps
  become: true
  roles:
    - role: openvpn-server
      vars:
        openvpn__version: 2.4.7
        openvpn__port: 11194
        openvpn__proto: udp4
        openvpn__dev: tun0
        openvpn__redirect-gateway: true
```

## To do

* add tasks to configure iptables
* add tasks to configure nat
