Sixpack ansible playbook
========================

Tested on Ubuntu 14.04/16.04/16.10 x64 EC2/DO/Vagrant.

# Usage

While creating EC2 instanse you got pem file, add it to ssh-agent:
```sh
`ssh-add <path_to_pem_file>`
```
To setup sixpack run:
```sh
ansible-playbook sixpack.yml -i '<ip_address>,' -u <username> -e 'sixpack_password=<password>'
```
Add `-k` if you need to connect with password.

# Development

Required Vagrant and VirtualBox.
```sh
vagrant up
```
