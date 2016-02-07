# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos7"

  config.vm.network "private_network", ip: "172.16.17.3"
  config.vm.hostname = "ansible-server"

  config.vm.provider "virtualbox" do |vb|
 
    # Customize the amount of memory on the VM:
    vb.memory = "512"
    vb.name = "ansible-server"
  end

  config.vm.provision "shell", inline: <<-SHELL
    yum -y upgrade
    yum -y install epel-release
    yum -y install ansible
  SHELL

end
