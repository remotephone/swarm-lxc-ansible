# docker-ubuntu-ansible
Install docker on ubuntu 16.04.3 with ansible

This playbook bootstraps a system and then installs docker. This currently just installs Docker-ce, it will eventually get a whole swarm up and running. 

## setup-swarm.yml
This playbook is basically the one available at https://github.com/nextrevision/ansible-swarm-playbook but I had to make some minor changes to detect the interface appropriately and format the docker swarm init command lines. Instead of selecting an interface, it queries the IP of the device and uses that and also i fixed the syntax to remove an "=" from the --advertise-addr flag. 