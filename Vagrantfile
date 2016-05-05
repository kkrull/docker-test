# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define 'docker-test'
  config.vm.box = 'phusion/ubuntu-14.04-amd64'
  config.vm.hostname = 'docker-test'
  config.vm.synced_folder "#{ENV['HOME']}/git", '/home/vagrant/git/'
  config.vm.synced_folder "#{ENV['HOME']}/.ssh", '/home/vagrant/host/ssh/'

  # Network accessible by the host
  config.vm.network 'private_network', 
    ip: '10.255.100.11',
    netmask: '255.255.255.0'

  config.vm.provision :shell, path: 'bootstrap.sh'
end

