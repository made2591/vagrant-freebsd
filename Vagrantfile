# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

   config.vm.guest = :freebsd
   config.vm.synced_folder ".", "/vagrant", id: "vagrant-root", disabled: true
   config.vm.box = "freebsd/FreeBSD-11.0-CURRENT"
   config.ssh.shell = "sh"
   config.vm.base_mac = "080027D14C66"

   config.vm.provider :virtualbox do |vb|
     vb.customize ["modifyvm", :id, "--memory", "1024"]
     vb.customize ["modifyvm", :id, "--cpus", "1"]
     vb.customize ["modifyvm", :id, "--hwvirtex", "on"]
     vb.customize ["modifyvm", :id, "--audio", "none"]
     vb.customize ["modifyvm", :id, "--nictype1", "virtio"]
     vb.customize ["modifyvm", :id, "--nictype2", "virtio"]
   end
end
