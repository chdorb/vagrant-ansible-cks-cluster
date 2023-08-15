# CKS Course cluster with Vagrant and Ansible

This setup is just a remake of [Kim Wuestkamp's lab setup on GCP for his CKS course](https://github.com/killer-sh/cks-course-environment).

This is a "just work on my laptop" first version, so fell free to open a PR to
improve if you update/adapt it to yours. ;-)

## Prerequisites

Works fine at this time (last commit date) on my two laptops with distro packages:

Fedora

* Fedora 37
* Vagrant 2.2.19
* vagrant-libvirt plugin 0.7.0
* Ansible 2.14

Archlinux

* Archlinux
* Vagrant 2.3.3
* vagrant-libvirt plugin 0.11.1 (not archlinux packaged, `vagrant plugin install`
* Ansible 2.14

There are some additionall collection to install for Ansible

```sh
ansible-galaxy collection install community.general ansible.posix kubernetes.core
```
