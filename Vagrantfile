# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.ssh.insert_key = false
  config.vm.define :centos_node1 do |node1|
    node1.vm.box = "centos1706_v3"
#    node1.vm.network "public_network", bridge: "eno1", ip:"192.168.131.102", netmask: "255.255.255.0"
    node1.vm.network :private_network, ip: "192.168.33.10"
    node1.vm.provider :virtualbox do |vb1|
      vb1.customize ["modifyvm", :id, "--memory", "1024","--cpus", "1", "--name", "centos_node1" ]
    end
  end

  config.vm.define :centos_node2 do |node2|
    node2.vm.box = "centos1706_v3"
#    node1.vm.network "public_network", bridge: "eno1", ip:"192.168.131.103", netmask: "255.255.255.0"
    node2.vm.network :private_network, ip: "192.168.33.11"
    node2.vm.provider :virtualbox do |vb2|
      vb2.customize ["modifyvm", :id, "--memory", "1024","--cpus", "1", "--name", "centos_node2" ]
    end
  end

  config.vm.define :centos_node3 do |node3|
    node3.vm.box = "centos1706_v3"
#    node1.vm.network "public_network", bridge: "eno1", ip:"192.168.131.104", netmask: "255.255.255.0"
    node3.vm.network :private_network, ip: "192.168.33.13"
    node3.vm.provider :virtualbox do |vb3|
      vb3.customize ["modifyvm", :id, "--memory", "1024","--cpus", "1", "--name", "centos_node3" ]
    end
  end
end
