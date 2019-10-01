# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  # config.vm.box_check_update = false

  config.vm.hostname = "ubuntu-01"

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true

    vb.name = "my_vm"
    # Customize the amount of memory on the VM:
    vb.memory = "1024"
    vb.cpus = "2"
  end

  # config.vm.network "forwarded_port", guest: 80, host: 8080
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  config.vm.network "private_network", ip: "192.168.33.10"
  # config.vm.network "public_network"

  config.vm.synced_folder "./html", "/usr/share/nginx/html"

  # config.vm.provision "shell", inline: <<-SHELL
  #   apt-get update
  #   apt-get install -y nginx
  # SHELL

  config.vm.provision "shell", path: "script.sh"
end
