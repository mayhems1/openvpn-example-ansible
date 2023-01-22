# OpenVPN server role

* Install and configure OpenVPN Server
* Generate keys for OpenVPN Server

## Vars

* `openvpn_base_dir` OpenVPN server config folder
* `openvpn_keys_dir` folder for keys
* `openvpn_port` OpenVPN server port
* `openvpn_proto` Protocol tcp/udp4
* `openvpn_dev` - tunnel device name
* `openvpn_redirect_gateway` - redirect default gateway to tunnel
* `openvpn_set_dns_servers` - DNS servers
* `openvpn_data_ciphers` - OpenVPN Cipher
* `openvpn_auth` - hash function
* `openvpn_tunnel_network` - network of VPN tunnel
* `openvpn_service_purpose` - description of a service
* `openvpn_version` - openvpn version
* `openvpn_package_name` - package name
* `openvpn_apt_repo_key` - key of repository
* `openvpn_repo` - URL repository
* `easyrsa_name` - package nage of EasyRSA
* `easyrsa_path` - path EasyRSA

## Example of a playbook

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
