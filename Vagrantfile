# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"

  config.hostmanager.manage_host = true
  config.hostmanager.manage_guest = true
  config.hostmanager.include_offline = true
  config.vm.hostname = "glpi.belbob.thuis"
  config.hostmanager.aliases = "glpi"
  config.vm.provision :hostmanager

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "site.yml"
  end

end
