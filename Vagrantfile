# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "chef/centos-6.6"

  config.vm.define :dev_vps do |node|
    node.vm.network "forwarded_port", guest: 80, host: 8080
    node.vm.network "private_network", ip: "192.168.33.100"

    node.vm.provision "ansible" do |ansible|
      ansible.playbook = "provision.yml"
    end
  end

end
