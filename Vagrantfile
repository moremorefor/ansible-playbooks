# -*- mode: ruby -*-
# vi: set ft=ruby :

ssh_port = 22
# ssh_port = COMMON_SSH_PORT

ssh_username = "vagrant"
# ssh_username = "COMMON_USER_NAME"

# ssh_key = "~/.ssh/id_rsa"

Vagrant.configure(2) do |config|
  config.vm.box = "chef/centos-6.6"

  config.vm.define :dev_server do |node|
    node.ssh.forward_agent = true
    node.ssh.username = ssh_username
    node.ssh.guest_port = ssh_port
    node.vm.network "private_network", ip: "192.168.33.100"
    node.vm.network "forwarded_port", guest: ssh_port, host: 2222, id: "ssh"
    # node.ssh.private_key_path = ssh_key
  end

end
