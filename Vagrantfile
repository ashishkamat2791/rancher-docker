# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

# Server-1 
Vagrant.configure("2") do |config|
 
   config.vm.define :rancher_server do |rancher_server|
    
  rancher_server.vm.box = "ubuntu/trusty64"
  rancher_server.vm.hostname = "rancher-server"

  rancher_server.vm.network "forwarded_port", guest: 8080, host: 8085
  rancher_server.vm.network "forwarded_port", guest: 3000, host: 3000
  rancher_server.vm.network "public_network", bridge: "Intel(R) 82579LM Dual Band Wireless-AC 7260" 
  rancher_server.ssh.forward_agent = true
   
  rancher_server.ssh.forward_agent = true

  rancher_server.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y wget
     wget  -qO- https://get.docker.com/|sh
	   docker run -d --restart=unless-stopped -p 8085:8080 rancher/server

    SHELL
  end

# Client-1
  config.vm.define :rancher_client1 do |rancher_client1|
    
  rancher_client1.vm.box = "ubuntu/trusty64"
  rancher_client1.vm.hostname = "rancher-client1"

  rancher_client1.vm.network "forwarded_port", guest: 8080, host: 8085
  rancher_client1.vm.network "forwarded_port", guest: 3000, host: 3000
  rancher_client1.vm.network "public_network", bridge: "Intel(R) 82579LM Dual Band Wireless-AC 7260" 
  rancher_client1.ssh.forward_agent = true
   
  rancher_client1.ssh.forward_agent = true

  rancher_client1.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y wget
     wget  -qO- https://get.docker.com/|sh
    
    SHELL
  end

 
 # Client -2
  config.vm.define :rancher_client2 do |rancher_client2|
    
  rancher_client2.vm.box = "ubuntu/trusty64"
  rancher_client2.vm.hostname = "rancher-client2"
  rancher_client2.vm.network "public_network", bridge: "Intel(R) 82579LM Dual Band Wireless-AC 7260" 
  rancher_client2.ssh.forward_agent = true
   
  rancher_client2.ssh.forward_agent = true

  rancher_client2.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y wget
     wget  -qO- https://get.docker.com/|sh
    
    SHELL
  end

#Client -3 
 config.vm.define :rancher_client3 do |rancher_client3|
    
  rancher_client3.vm.box = "ubuntu/trusty64"
  rancher_client3.vm.hostname = "rancher-client3"
  rancher_client3.vm.network "public_network", bridge: "Intel(R) 82579LM Dual Band Wireless-AC 7260" 
  rancher_client3.ssh.forward_agent = true
   
  rancher_client3.ssh.forward_agent = true

  rancher_client3.vm.provision "shell", inline: <<-SHELL
     apt-get update
     apt-get install -y wget
     wget  -qO- https://get.docker.com/|sh
    
    SHELL
  end
end  