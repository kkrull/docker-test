# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = 'phusion/ubuntu-14.04-amd64'
  config.vm.define 'docker-test' do |vm_config|
    vm_config.vm.hostname = 'docker-test'
  end

  config.vm.synced_folder '../share', '/home/vagrant/src/'

  # Network accessible by the host
  config.vm.network 'private_network', 
    ip: '10.255.100.11',
    netmask: '255.255.255.0'

  config.vm.provision :shell, path: 'bootstrap.sh'
end

