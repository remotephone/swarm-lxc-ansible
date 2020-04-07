# swarm-lxc-ansible

Install docker on debian 10 with ansible. Also install docker swarm.

This playbook bootstraps a system and then installs docker. This currently just installs Docker-ce, I run the two playbooks separately. 

## setup-swarm.yml
This playbook is basically the one available at https://github.com/nextrevision/ansible-swarm-playbook but I had to make some minor changes to detect the interface appropriately and format the docker swarm init command lines. Instead of selecting an interface, it queries the IP of the device and uses that and also i fixed the syntax to remove an "=" from the --advertise-addr flag. 
