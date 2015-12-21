# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |machine|
  machine.vm.box = "ansible_docker"
  machine.vm.box_url =  "https://oss-binaries.phusionpassenger.com/vagrant/boxes/latest/ubuntu-14.04-amd64-vbox.box"

  machine.vm.define :docker do |config|
    config.vm.network :private_network, :ip => "10.0.0.115"
    config.vm.host_name = "docker"

    config.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
    SHELL

    config.vm.provision :ansible do |ansible|
      ansible.playbook = "provisioning/docker.yml"
      ansible.verbose = "vvv"
    end
  end
end
