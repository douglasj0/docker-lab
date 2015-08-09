# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.define 'centos-docker1' do |node|
    node.vm.hostname = "centos-docker"
    node.vm.box = "chef/centos-7.0"
    mem = 512
    cpus = 2
    node.vm.network "private_network", ip: "10.10.2.11"
    node.vm.provider "virtualbox" do |vbox|
      vbox.gui = false
      vbox.memory = mem
      vbox.cpus = cpus
    end
    #config.vm.provision "shell", inline: "sudo yum -y update"
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/site.yml"
    end
  end # centos-docker1

  config.vm.define 'centos-docker2' do |node|
    node.vm.hostname = "centos-docker"
    node.vm.box = "chef/centos-7.0"
    mem = 512
    cpus = 2
    node.vm.network "private_network", ip: "10.10.2.12"
    node.vm.provider "virtualbox" do |vbox|
      vbox.gui = false
      vbox.memory = mem
      vbox.cpus = cpus
    end
    #config.vm.provision "shell", inline: "sudo yum -y update"
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/site.yml"
    end
  end # centos-docker2

  config.vm.define 'ubuntu-docker1' do |node|
    node.vm.hostname = "ubuntu-docker"
    node.vm.box = "ubuntu/trusty64"
    mem = 512
    cpus = 2
    node.vm.network "private_network", ip: "10.10.2.21"
    node.vm.provider "virtualbox" do |vbox|
      vbox.gui = false
      vbox.memory = mem
      vbox.cpus = cpus
    end
    config.vm.provision "shell", inline: "sudo apt-get -y update"
    #config.vm.provision "shell", inline: "sudo apt-get -y upgrade"
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/site.yml"
    end
  end # ubuntu-docker1

  config.vm.define 'ubuntu-docker2' do |node|
    node.vm.hostname = "ubuntu-docker"
    node.vm.box = "ubuntu/trusty64"
    mem = 512
    cpus = 2
    node.vm.network "private_network", ip: "10.10.2.22"
    node.vm.provider "virtualbox" do |vbox|
      vbox.gui = false
      vbox.memory = mem
      vbox.cpus = cpus
    end
    config.vm.provision "shell", inline: "sudo apt-get -y update"
    #config.vm.provision "shell", inline: "sudo apt-get -y upgrade"
    config.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/site.yml"
    end
  end # ubuntu-docker2

end
