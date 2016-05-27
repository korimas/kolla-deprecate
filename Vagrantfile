# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "controller" do |controller|
    controller.vm.box = "ubuntu/trusty64"
    controller.vm.network "forwarded_port", guest: 80, host: 8088
    controller.vm.network "private_network", ip: "20.0.2.11"
    controller.vm.network "private_network", ip: "30.0.2.11"
    controller.vm.hostname = "controller"
    controller.vm.provider "virtualbox" do |v|
      v.memory = 8192
      v.cpus = 4
    end
  end

  config.vm.define "compute" do |controller|
    controller.vm.box = "ubuntu/trusty64"
    controller.vm.network "private_network", ip: "20.0.2.12"
    controller.vm.network "private_network", ip: "30.0.2.12"
    controller.vm.hostname = "compute"
    controller.vm.provider "virtualbox" do |v|
      v.memory = 8192
      v.cpus = 4
    end
  end

end
