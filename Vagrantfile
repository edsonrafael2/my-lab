# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "server1" do |server1|
    server1.vm.box = "ubuntu/focal64"
    server1.vm.network "public_network", ip:"192.168.100.20", bridge: "wlp9s0"
    server1.vm.provision "shell", path:"script.sh"
    end
  config.vm.define "server2" do |server2|
    server2.vm.box = "centos/7"
    server2.vm.network "public_network", ip:"192.168.100.21", bridge:"wlp9s0"
    end
  config.vm.define "server3" do |server3|
    server3.vm.box = "debian/buster64"
    server3.vm.network "public_network", ip:"192.168.100.22", bridge:"wlp9s0"
    end
end
