# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "campusSportswear"
  config.vm.box_url = "campusSportswear.box"

  config.vm.network :private_network, ip: "192.168.33.10"
  # config.vm.network :public_network
  config.ssh.username = "vagrant"

  config.vm.provider "virtualbox" do |v|
     v.customize ["modifyvm", :id, "--memory", 3092, "--cpus", 2, "--name", "CampusSportswear"]
  end

  config.vm.synced_folder "..", "/campusSportswear", :owner => "apache", :group => "apache", :mount_options => ["dmode=777,fmode=777"]
end
