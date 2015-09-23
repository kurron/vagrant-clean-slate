# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "public_network"
  config.vm.hostname = "clean-slate"
  config.ssh.username = "vagrant"
  config.ssh.password = "vagrant"
# config.ssh.forward_agent = true
# config.ssh.forward_x11 = true

  config.vm.provider "virtualbox" do |v|
      v.gui = false
      v.customize ["modifyvm", :id, "--rtcuseutc", "on"]
      v.customize ["modifyvm", :id, "--hwvirtex", "on"]
      v.customize ["modifyvm", :id, "--nestedpaging", "on"]
      v.customize ["modifyvm", :id, "--vtxvpid", "on"]
      v.customize ["modifyvm", :id, "--largepages", "on"]
      v.customize ["modifyvm", :id, "--acpi", "on"]
      v.customize ["modifyvm", :id, "--nictype1", "virtio"]
      v.customize ["modifyvm", :id, "--groups", "/Clean Slate"]
      v.customize ["modifyvm", :id, "--memory", "5120"]
      v.customize ["modifyvm", :id, "--vram", "24"]
      v.customize ["modifyvm", :id, "--cpus", "2"]
  end
end
