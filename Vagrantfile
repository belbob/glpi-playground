# -*- mode: ruby -*-
# vi: set ft=ruby :

#require 'yaml'
#settings = YAML.load_file './roles/common/defaults/main.yml'

# Get fqdn and alias from iventory file hosts
HOSTS_DATA = IO.readlines("./hosts")
HOST1 = HOSTS_DATA[1]
SPLIT_HOSTS1_DATA = HOST1.split(" ")
FQDN = SPLIT_HOSTS1_DATA.first
SPLIT_FQDN = FQDN.split(/\./)
ALIAS = SPLIT_FQDN.first

#FQDN = "glpi.belbob.thuis"
#ALIAS = "glpi"

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"

  config.hostmanager.manage_host = true
  config.hostmanager.manage_guest = false
  config.hostmanager.include_offline = true
  config.vm.hostname = FQDN
  config.hostmanager.aliases = ALIAS

  config.vm.provision :hostmanager

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "Vagrant_site.yml"
  end

end
