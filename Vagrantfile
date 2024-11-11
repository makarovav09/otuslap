# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"
  config.vm.box_version = "20241002.0.0"
  config.vm.box_check_update = false
  config.vm.hostname = "test1"
  config.vm.define "test1"
  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"
  # config.vm.synced_folder "../data", "/vagrant_data"
  # config.vm.synced_folder ".", "/vagrant", disabled: true
   config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     # vb.gui = true
  
    # Customize the amount of memory on the VM:
    vb.memory = "2048"
    vb.name = "test1"
    vb.cpus = "2"
   end
   config.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install --install-recommends linux-generic-hwe-22.04 -y
      reboot
   SHELL
end
