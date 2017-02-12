# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"
  config.vm.hostname = "manifoldcf"
  config.vm.network "forwarded_port", guest: 5432, host: 8432
  config.vm.network "forwarded_port", guest: 8345, host: 7345
  config.vm.network "forwarded_port", guest: 22, host: 55
  config.vm.network "private_network", ip: "192.168.33.66"

  config.vm.provider "virtualbox" do |vb|
     vb.memory = "4096"
  end

  #config.vm.define 'manifoldcf' do |machine|

   # machine.vm.provision 'ansible' do |ansible|
    #    ansible.playbook = 'mcf-agents.yml'
     #   ansible.sudo = true
      #  ansible.inventory_path = 'dev'
       # ansible.host_key_checking = false
    #end

  #end

  #x11
  config.ssh.forward_x11 = true

end
