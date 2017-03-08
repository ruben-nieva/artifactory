# -*- mode: ruby -*-
# vi: set ft=ruby :

# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

## Setup for Openshif master server
  config.vm.define "jfrog" do |jfrog|
      jfrog.vm.hostname = "cicd"
      jfrog.vm.box = "ubuntu/trusty64"
      #jfrog.ssh.insert_key = false
      jfrog.vm.provider "virtualbox" do |vb|
         vb.memory = "1524"
         vb.cpus = "2"
      end
      jfrog.vm.network "private_network", ip: "10.2.2.3"
      jfrog.vm.provision :shell, :path => "scripts/jfrog.sh"
      # artifactory
      #jfrog.vm.network :forwarded_port, guest: 8081, host: 8081
  end


end
