# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "arnemertz/Xubuntu16.04"

  config.vm.provider :virtualbox do |v|
    v.name = "i3"
    v.gui = true
    v.memory = 4096
    v.cpus = 2
    v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
    v.customize ["modifyvm", :id, "--ioapic", "on"]
    v.customize ["modifyvm", :id, "--hwvirtex", "on"]
    v.customize ["modifyvm", :id, "--accelerate3d", "on"]
	  v.customize ['modifyvm', :id, '--clipboard', 'bidirectional']
  end

  config.vm.hostname = "i3"
  #config.vm.network :private_network, ip: "192.168.33.27"

  # Ansible provisioner.
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "vagrant.yml"
    ansible.verbose = "v"
    ansible.sudo = true
  end

end
