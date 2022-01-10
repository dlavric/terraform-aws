# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
    config.vm.box = "hashicorp/bionic64"

    

    config.vm.define "terraform" do |terraform|
        terraform.vm.hostname = "terraform"
        terraform.vm.network "private_network", ip: "192.168.56.41"
        terraform.vm.provider "virtualbox" do |v|     
            v.memory = 1024 * 4
            v.cpus = 2  
    end

    terraform.vm.provision "shell", path: "scripts/install_terraform.sh"
    
    end  


# Install Azure CLI and setup azure env variables

    #config.vm.provision "file", source: "scripts/azurerm.sh", destination: "/home/vagrant/azurerm.sh"
    #config.vm.provision "shell", inline: "cat /home/vagrant/azurerm.sh >> /home/vagrant/.bashrc"
    #config.vm.provision "shell", path: "scripts/install_azurecli.sh"

# Install AWS CLI 

    config.vm.provision "shell", path: "scripts/install_awscli.sh"

end