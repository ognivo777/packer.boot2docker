# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "file://./packer_virtualbox-iso_virtualbox.box"
  config.vm.box_check_update = false

  config.vm.network "private_network", ip: "192.168.56.105", nic_type: "virtio", auto_config: false

  config.vm.synced_folder "./", "/home/docker/sync", id: "docker", :nfs => true,  :mount_options   => ['nolock,vers=3,udp']

  config.vm.provider "virtualbox" do |vb|
    vb.name = "vagrant_boot2docker"
    vb.gui = true
    vb.memory = "2048"
    vb.cpus = 2
  end
  
  config.ssh.username="docker"
  config.ssh.password="tcuser"
  config.ssh.shell="/bin/sh -l"

end
