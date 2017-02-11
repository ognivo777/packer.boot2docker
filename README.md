# packer.boot2docker
HashiCorp Packer build for boot2docker persistance VM image for VirtualBox. Created virtual appliance booting from HDD and has persistant */opt* and */home* folders. Also installed extensions will not remove after reboot.

This VM is very small (~50Mb) and useful for developers, who wants to play with Docker.

####Requirements
* [Packer](#packer) 
* [VirtualBox](#virtualbox)

# Usage
* `git clone https://github.com/ognivo777/packer.boot2docker.git`
* `cd packer.boot2docker`
* [Download latest release boot2docker.iso](https://github.com/boot2docker/boot2docker/releases/latest) and place near boot2docker.json
* Open boot2docker.json and fix "iso_checksum" using actual value from download page
* Run Packer: `packer build boot2docker.json`

After building complete *boot2docker_template.ova* appears in *output-virtualbox-iso* folder.
