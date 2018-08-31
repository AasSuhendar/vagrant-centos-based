# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # General Vagrant VM configuration.
  config.vm.box = "centos/7"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  
  config.ssh.private_key_path = File.expand_path('~/.vagrant.d/insecure_private_key')
  config.ssh.insert_key = false
  
  config.vm.provider :virtualbox do |v|
    v.memory = 512
    v.linked_clone = true
  end

  # Application 0.
  config.vm.define "tower.lab.example.com" do |app|
    app.vm.hostname = "servera.lab.example.com"
    app.vm.network :private_network, ip: "192.168.103.117"
  end

  # Application 1.
  config.vm.define "servera.lab.example.com" do |app|
    app.vm.hostname = "servera.lab.example.com"
    app.vm.network :private_network, ip: "192.168.103.118"
  end

  # Application 2.
  config.vm.define "serverb.lab.example.com" do |app|
    app.vm.hostname = "serverb.lab.example.com"
    app.vm.network :private_network, ip: "192.168.103.119"
  end

  # Application 3.
  config.vm.define "serverc.lab.example.com" do |app|
    app.vm.hostname = "serverc.lab.example.com"
    app.vm.network :private_network, ip: "192.168.103.120"
  end

  # Application 4.
  config.vm.define "serverd.lab.example.com" do |app|
    app.vm.hostname = "serverd.lab.example.com"
    app.vm.network :private_network, ip: "192.168.103.121"
  end

end
