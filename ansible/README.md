
Set up a single node kubernetes cluster with flannel.

## REQUIREMENTS

Host machine should run debian 11 with more than 2 vCPU and 2mB RAM

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

- [Kubernetes Setup](https://www.redpill-linpro.com/techblog/2019/04/04/kubernetes-setup.html)
- [Kuberentes on Ubuntu](https://www.fosstechnix.com/how-to-install-kubernetes-cluster-on-ubuntu/)
- [Install kubernetes cluster on debian](https://www.linuxtechi.com/install-kubernetes-cluster-on-debian/)
