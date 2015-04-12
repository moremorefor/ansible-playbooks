# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "chef/centos-6.6"

  config.vm.define :dev_server do |node|
    node.ssh.forward_agent = true
    node.vm.network "forwarded_port", guest: 80, host: 8081
    node.vm.network "private_network", ip: "192.168.33.100"

  end

end
