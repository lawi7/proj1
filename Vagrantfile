# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.ssh.insert_key = false
  config.vm.box = "bento/ubuntu-20.04"

   config.vm.network "forwarded_port", guest: 80, host: 8080
   config.vm.network "forwarded_port", guest: 443, host: 8443
   config.vm.hostname = "testserver1"
   config.vm.network "private_network", ip: "192.168.33.10"

   config.vm.synced_folder "pub", "/var/www/html/pub"
   config.vm.synced_folder "src", "/var/www/src"

   config.vm.provider "virtualbox" do |vb|
     vb.memory = "1024"
   end
  #
  #  config.vm.provision "ansible" do |ansible|
  #    ansible.verbose = "v"
  #    ansible.playbook = "setup.yaml"
  #  end
end
