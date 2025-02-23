# CKS Course cluster with Vagrant and Ansible

This setup is just a remake of [Kim Wuestkamp's lab setup on GCP for his CKS course](https://github.com/killer-sh/cks-course-environment).

This is a "just work on my laptop" first version, so fell free to open a PR to
improve if you update/adapt it to yours. ;-)

## Prerequisites

Works fine at this time (last commit date) on my two laptops with distro packages:

Fedora

* Fedora 40
* Vagrant 2.3.4
* vagrant-libvirt plugin 0.11.2
* Ansible 2.16

Archlinux

* Archlinux
* Vagrant 2.3.3
* vagrant-libvirt plugin 0.11.1 (not archlinux packaged, `vagrant plugin install`)
* Ansible 2.14

Ubuntu

* Ubuntu 24.04
* Vagrant 2.4.3
* vagrant-libvirt plugin 0.12.2
* Ansible 2.16.3

There are some additional collections to install for Ansible

```sh
ansible-galaxy collection install community.general ansible.posix kubernetes.core
```
