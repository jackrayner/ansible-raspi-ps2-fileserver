# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  # Raspberry Pi OS is currently based on Debian Buster.
  config.vm.box = "debian/buster64"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "ansible-raspi-ps2-fileserver"
    vb.gui = false
    vb.cpus = "2"
    vb.memory = "2048"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end
