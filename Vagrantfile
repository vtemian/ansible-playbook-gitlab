# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "hashicorp/precise64"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "gitlab.yml"
    ansible.verbose = "vvv"
  end

  config.vm.network "forwarded_port", guest: 80, host: 8001

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
  end

end
