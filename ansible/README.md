# Vagrant file for build boot2docker with Ansible
I realy love boot2docker project. This is simplest way to dive into Docker under Windows. So offen Ansible used for provision containers and docker infrastructure.
This vagrant file describes smallest VM (about 120Mb) with Docker and Ansible inside for every day use by developers.

#### Requirements
* [Vagrant](https://www.vagrantup.com/) 
* [VirtualBox](https://www.virtualbox.org/)
* **packer_virtualbox-iso_virtualbox.box** - created with packer using config on parent folder.

#### Usage
```
git clone https://github.com/ognivo777/packer.boot2docker.git
cd packer.boot2docker/ansible
vagrant up
```

Then you can ssh into created vm:

`vagrant ssh`

and check ansible:

`ansible -i "localhost ansible_python_interpreter=/usr/local/bin/python" -m setup localhost -u docker`
