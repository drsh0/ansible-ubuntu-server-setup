# ansible-ubuntu-server-setup
Ansible scripts to set up a ubuntu server for general usage + docker. Currently, this sets up:

* preferred packages
* unattended upgrades
* secures SSH
* sets up zsh
* installs docker

## Instructions

1. install ubuntu server on target
2. ensure a host system can SSH to target
3. install ansible on host via `sudo apt install ansible`
4. edit `/etc/ansible/hosts` to include host and IP of target system
5. clone this repo via `git clone git@github.com:drsh0/ansible-ubuntu-server-setup.git`
6. `cd ansible-ubuntu-server-setup`
7. initiate ansible playbook on target host: `ansible-playbook server-setup.yml -K`
8. supply sudo password for target when requested
9. let the playbook run