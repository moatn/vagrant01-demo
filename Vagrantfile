# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|
    config.ssh.insert_key = false

    # set default settings
    config.vm.box = "ubuntu/bionic64"
    config.vm.provider "virtualbox" do |vb|
        vb.memory = 1024
        vb.cpus = 1
    end

    config.vm.define :web01, primary: true do |machine|
        machine.vm.host_name = "web01.local"
        machine.vm.network "private_network", ip: "192.168.50.10"

        machine.vm.provider "virtualbox" do |vb|
            vb.cpus = 1
        end

        # sync web01 to /home/vagrant/ansible
        machine.vm.synced_folder "web01/", "/home/web01/"

        # upload vagrant private key to ansible controller
        machine.vm.provision "file", source: "~/.vagrant.d/insecure_private_key", destination: "$HOME/.ssh/id_rsa"
    end
end