# Description

This is a sample set of configs to create virtual machine "api-vm" by Vagrant 
and provision it by Ansible. It prepares [this project](https://github.com/Trofogol/sample-http-api) to run via uWSGI (launched as daemon).

## Requirements

> Built on Ubuntu 18

- Python3
- [Vagrant](https://www.vagrantup.com/intro/getting-started/install.html)
- Any hypervisor that Vagrant can work with (project was built on [VirtualBox](https://www.virtualbox.org/))
- Ansible (*It's better install it as Python3 pip module*)

## Structure

#### Vagrantfile

Contains configuration for Vagrant VM.

#### test_corp-dump.sql

MySQL database dump. It is needed to run my 
[sample API project](https://github.com/Trofogol/sample-http-api) correctly. 
Unpacks by Ansible during VM provision.

#### ansible-provision/

Contains Ansible playbook and roles for VM provision. It lacks Ansible 
inventory file because Vagrant 
[generates it by itself](https://www.vagrantup.com/docs/provisioning/ansible_intro.html#auto-generated-inventory).
