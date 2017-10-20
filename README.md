# vagrant-ansible-docker
Install Docker on CentOS 7 using vagrant environment and ansible tool

### Before provisioning

- prepare two vagrant servers, one with ansible software and another for testing.
- example configuration for vagrant servers is in the Vagrantfile

- perform login ability on the machine without using password (only with key)

### Usage

`
$ ansible-playbook provision.yml
