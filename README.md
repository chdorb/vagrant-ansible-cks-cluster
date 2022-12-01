# CKS Course cluster with Vagrant and Ansible

This setup is just a remake of [Kim Wuestkamp's lab setup on GCP for his CKS course](https://github.com/killer-sh/cks-course-environment).

This is a "just work on my laptop" first version, so fell free to open a PR to
improve if you update/adapt it to yours. ;-)

## Prerequisites

Works fine at this time (last commit date) on Fedora 36 with:
* Vagrant 2.2.19 with libvirt provider
* Ansible 2.12

There are some additionall collection to install for Ansible

```sh
ansible-galaxy collection install community.general ansible.posix kubernetes.core
```
