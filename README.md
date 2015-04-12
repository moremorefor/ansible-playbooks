# Ansible Playbooks

- Ansible 1.8.4
- CentOS 6.6
- Vagrant (optional)

### Setup
Edit for your environment.
- group_vars/all
- hosts
- site.yml

### Getting started
```
$ vagrant up
```

### Provisioning with ansible command
```
$ vagrant ssh-config > ssh.config
$ ansible-playbook -i flask/hosts flask/site.yml
```
