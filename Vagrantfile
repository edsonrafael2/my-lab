# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "server1" do |server1|
    server1.vm.box = "ubuntu/focal64"
    server1.vm.network "public_network", ip:"192.168.100.20", bridge: "wlp9s0"
    server1.vm.provision "shell", path:"script.sh"
    server1.vm.provider "virtualbox" do |vm|
      vm.name = "ubuntu-server1"
      vm.memory = 2048
    end
  end
  config.vm.define "server2" do |server2|
    server2.vm.box = "centos/7"
    server2.vm.network "public_network", ip:"192.168.100.21", bridge:"wlp9s0"
    server2.vm.provider "virtualbox" do |vm|
      vm.name = "centos7-server2"
    end 
  end
  config.vm.define "server3" do |server3|
    server3.vm.box = "debian/buster64"
    server3.vm.network "public_network", ip:"192.168.100.22", bridge:"wlp9s0"
    server3.vm.provider "virtualbox" do |vm|
      vm.name = "debian10-server3"
    end
  end

  config.vm.define "server4" do |server4|
    server4.vm.box = "fedora/38-cloud-base"
    server4.vm.network "public_network", ip: "192.168.100.23", bridge:"wlp9s0"
    server4.vm.provider "virtualbox" do |vm|
      vm.name = "fedora38-server4"
    end
  end
end
