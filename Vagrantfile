# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
    
  config.ssh.insert_key = false

  config.vm.define "client1" do |client1|
    client1.vm.box="centos/7"
    client1.vm.hostname = "client1.bolocal"
    client1.vm.network :private_network, ip: "192.168.1.101", :netmask => "255.255.255.255"
  end

  config.vm.define "client2" do |client2|
    client2.vm.box="centos/7"
    client2.vm.hostname = "client2.bolocal"
    client2.vm.network :private_network, ip: "192.168.1.102", :netmask => "255.255.255.255"
  end
  
  config.vm.define "client3" do |client3|
    client3.vm.box = "centos/7"
    client3.vm.hostname = "client3.bolocal"
    client3.vm.network :private_network, ip: "192.168.1.103", :netmask => "255.255.255.255"
  end

  config.vm.provision "ansible" do |ansible|
        ansible.playbook = "playbook.yml"
  end

end
