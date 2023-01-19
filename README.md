# OpenVPN Server at a VPS

Ansible roles and playbooks for OpenVPN Server at a VPS

## Requirements

* VPS with Linux Debian based distr
* SSH access
* sudo / root access

## Roles

* roles/openvpn-server - Install and basic configuration of OpenVPN Server
* roles/iptables - configuration iptables

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
