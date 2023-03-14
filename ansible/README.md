
## SETTING UP FOR DEVELOPMENT

Copy the example `hosts.example` file and fill out necessary fields
```sh
cp hosts.example hosts
```

## PREREQUISITES

Ensure the host has ssh connection as well as a dev user created with sudo priviledges:
```
useradd -G sudo -s /usr/bin/bash -m dev
passwd dev
```

On the local system, install ssh key (might need enable `PubKeyAuthentication` in `/etc/ssh/sshd_config`):
```
ssh-copy-id dev@<host>
```

## RUNNING PLAYBOOKS
```
ansible-playbook --ask-become-pass website.yml
```

## RESOURCES
- [ansible playbook best practices](https://docs.ansible.com/ansible/2.8/user_guide/playbooks_best_practices.html)
- [ansible hardening](https://www.redhat.com/sysadmin/harden-new-system-ansible)

