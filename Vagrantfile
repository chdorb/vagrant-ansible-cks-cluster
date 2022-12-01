# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
IMAGE_NAME = "generic/ubuntu1804"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provider "libvirt" do |libvirt|
    libvirt.cpus = 2
    libvirt.memory = 4096
  end

  hosts = ["master", "worker"]
  hosts.each do |host|
    config.vm.define "cks-#{host}" do |system|
      system.vm.box = IMAGE_NAME
      system.vm.hostname = "cks-#{host}"
      system.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook-#{host}.yml"
        # ansible.verbose = "v"
      end
    end
  end
end
