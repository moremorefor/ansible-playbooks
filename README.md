# Ansible Playbooks

- Ansible 1.8.4
- CentOS 6.6
- Vagrant

### Setup
Edit for your environment.
- group_vars/all
- inventory/hosts

### Getting started
1. Setup server

  ```
  $ vagrant up
  $ vagrant ssh-config > ssh.config
  $ ansible-playbook -i logpot/inventory/hosts logpot/setup.yml
  ```

1. Change ssh settings in Vagrantfile

  Edit `ssh_port`, `ssh_username`, `ssh_key` and, uncomment `private_key_path`.

1. Delete `private_key`

  ```
  $ rm -f .vagrant/machines/dev_server/virtualbox/private_key
  ```

1. Reload Vagrant settings

  ```
  $ vagrant reload
  ```

1. Setup application environment

  ```
  $ vagrant ssh-config >! ssh.config
  $ ansible-playbook -i logpot/inventory/hosts logpot/app.yml
  ```
