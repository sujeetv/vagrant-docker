# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.define :manager1 do |manager1|
    # config.vm.network "forwarded_port", guest: 80, host: 8080
    manager1.vm.network "private_network", ip: "192.168.33.10"
    # config.vm.network "public_network"
    # config.vm.synced_folder "../data", "/vagrant_data"
    manager1.vm.provider "virtualbox" do |vb|
    #   # Display the VirtualBox GUI when booting the machine
    #   vb.gui = true
    #
    #   #Customize the amount of memory on the VM:
       vb.memory = "1024"
    end
  end
  config.vm.define :worker1 do |worker1|
    worker1.vm.network "private_network", ip: "192.168.33.11"
  end
end
