ansible-cis
=========

This role applies the CIS benchmarks for Ubuntu 16.04. This is copied almost verbatim from https://github.com/awailly/cis-ubuntu-ansible
and Uber's mountopts https://github.com/Uberspace/ansible-mountopts

Requirements
------------

There are no requirements but this role has only been tested on Ubuntu 16.04.

Role Variables
--------------

```
lxd_container: True

partitioning: True
use_aide: False
set_bootloader_password: false
grub_superuser: root
root_password_grub: grub.pbkdf2.sha512.10000.2EDB88EB8D897897A67D45961EFACF9878E3280CC9FCE3BD0035D0F789409BC698831ED38349DF008FC9B1FCF56B26997BB802ED0299B0480744DD45C8658F18.516ABD49F2E70BF3EE21D02B5F6FBFBDC47C056B4CC8FEF2AB83E5F0997C1B00963E11A2B83533D892B3D64FDA2A065AF966D92F029402CB5E3BFD3776FE3D0C 
root_password: $6$22JQUvbd$n9xjZ9mM4todclTzHHUyIlmlxrlXIXFS4H4baITVFqGn.hzo6o.m4lIk.3cPD.ftqkfHctBZzJxR4pSqV8MEL/ 
enable_aslr: True
enable_selinux: True
use_apparmor: True
selinux_apparmor: apparmor
apt_upgrade: True
apt_cache_valid_time: 3600
ntp_package: chrony
remove_xserver: True
net_ipv4_ip_forward: 0
enable_tcp_syncookies: True
disable_ipv6: True
enable_hosts_allow: False
enable_hosts_deny: False
activate_iptables: True
iptables_rules_file: /etc/iptables/rules.v4
firewall_policy_drop: True
disable_wifi: True
enable_auditd: True
max_log_file_auditd: 200
set_rsyslog_remote: True
syslog_package: rsyslog
remote_logs_host_address: 192.168.112.1
restrict_core_dumps: True
permit_root_login: without-password
sshd_allow_users: sshuser
sshd_allow_groups: sshusersallow
sshd_deny_users: sshdenied
sshd_deny_groups: sshusersdeny
dpkg_verify: False
lock_shadow_accounts: False
modify_user_homes: True
ntp_server: 192.168.1.2
```

Dependencies
------------

None.

Example Playbook
----------------
```
- hosts: hypervisors
  roles:
    - ansible-cis
```
License
-------

MIT

Author Information
------------------

Phil Dorczuk - codedcompliance@yahoo.com

