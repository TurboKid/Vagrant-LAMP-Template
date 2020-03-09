# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.hostname = "benchmark"
  config.vm.network "forwarded_port", host: 8080, guest: 80
  config.vm.network "forwarded_port", host: 3306, guest: 3306
  config.vm.network "private_network", ip: "192.168.33.111"
  config.vm.provision :shell, path: "Vagrant.bootstrap.sh"
  config.vm.synced_folder "www/", "/var/www/html"
end
