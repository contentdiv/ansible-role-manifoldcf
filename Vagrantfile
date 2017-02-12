# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"
  config.vm.hostname = "manifoldcf"
  config.vm.network "forwarded_port", guest: 5432, host: 9432
  config.vm.network "forwarded_port", guest: 8345, host: 9345
  config.vm.network "forwarded_port", guest: 22, host: 55
  config.vm.network "private_network", ip: "192.168.33.55"

  config.vm.provider "virtualbox" do |vb|
     vb.memory = "4096"
  end

  #x11
  config.ssh.forward_x11 = true

end
