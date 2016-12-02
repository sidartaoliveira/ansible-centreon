# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(2) do |config|
  config.vm.box = "centos/6"

  config.vm.network "forwarded_port", guest: 80, host: 8080
   
  config.vm.provision "shell", inline: <<-SHELL
    bash -x <( wget --quiet https://gist.githubusercontent.com/sidartaoliveira/65da9c05b54012ba7e968811086ebc5a/raw/f6d8653a080dcb814344c71c6af788de801e9039/centreon-install-vagrant-centos6 -O - ) 
   SHELL
end
