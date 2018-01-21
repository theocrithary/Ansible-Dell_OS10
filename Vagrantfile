# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define "mgmt" do |mgmt|
    mgmt.vm.box = "mgmt"
    mgmt.vm.box_url = "file://centos65-x86_64-20140116.box"
    mgmt.vm.hostname = "mgmt"
    mgmt.vm.network "private_network", ip: "192.168.56.10"
  end

  config.vm.provision "shell", inline: <<-SHELL
    yum -y install ansible
  SHELL
end
