# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"
IMAGE_NAME = "generic/ubuntu2004"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.provider "libvirt" do |libvirt|
    libvirt.cpus = 2
    libvirt.memory = 2048
  end

  hosts = ["master", "worker"]
  hosts.each do |host|
    config.vm.define "cks-#{host}" do |system|
      system.vm.box = IMAGE_NAME
      system.vm.hostname = "cks-#{host}"
      system.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook-#{host}.yml"
        ansible.groups = {
         "master" => ["master"],
         "workers" => ["worker"]
        }
        # use ansible.verbose for debugging purpose
        # ansible.verbose = "v"
        # Kubernetes previous version
        # uncomment ansible.extra_vars to work on k8s upgrade topic
        # ansible.extra_vars = {
        #   kubernetes: {
        #     version: "1.29.0"
        #   }
        # }
      end
    end
  end
end
