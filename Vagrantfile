# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
 
  config.vm.box = "geerlingguy/ubuntu2004"
  
  config.ssh.insert_key = false
  
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  config.vm.provider :virtualbox do |v|
	v.memory = 1024
	v.linked_clone = true
  end
 
 #app server
  config.vm.define "app1" do |app|
	app.vm.hostname = "orc-app1.test"
	app.vm.network :private_network, ip: "192.168.1.102"
  end
end
  
