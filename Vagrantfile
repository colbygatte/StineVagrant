# -*- mode: ruby -*-
# vi: set ft=ruby :
# https://docs.vagrantup.com.
# boxes: https://atlas.hashicorp.com/search.

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/trusty64"
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.network :forwarded_port, guest: 80, host: 8080
  config.vm.synced_folder ".", "/vagrant", :mount_options => ["dmode=777","fmode=666"]
  
  config.vm.provider "virtualbox" do |vb|
     vb.memory = "3000"
  end
end
