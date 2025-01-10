This playbooks for management iptables on ubuntu server.

Both playbooks do the same, creates 3 chains with rules:

  1st chain monitoring for ports [8082,8345, 5252] and allow 10 random ip, the rest reject.

  2nd chain ssh-protect for access [ 22,2244] and allow 10 random ip from network 192.168.4.0/24, the rest drop.

  3rd chain app_protect for application port protection [ 6073, 8080, 4670] and allow 10 random ip from network 192.168.4.0.0/24, the rest reject. 

iptables_module.yml Using module ansible.builtin.iptables. This module does not handle the saving and/or loading of rules, but rather only manipulates the current rules that are present in memory. This is the same as the behaviour of the iptables and ip6tables command which this module uses internally. But im save changes to file.

iptables_persistent.yml Using iptables-restore and manage iptables rules from file.

[![Ansible for DevOps Cover](https://s3.amazonaws.com/titlepages.leanpub.com/ansible-for-devops/medium)](https://www.ansiblefordevops.com/)

[![TEST img](https://ibb.co/F419LxS)

[![TEST img2](https://i.ibb.co/image.png)]

