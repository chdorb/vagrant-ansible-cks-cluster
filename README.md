# CKS Course cluster with Vagrant and Ansible

This is a "just work on my laptop" first version, so fell free to open a PR to
improve if you update/adapt it to yours. ;-)

## Prerequisites

* Vagrant with libvirt provider 
* Ansible 2.9

There are some additionall collection to install for Ansible

```sh
ansible-galaxy collection install community.general ansible.posix kubernetes.core
```
