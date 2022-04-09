# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  ## Escolha da Box
  config.vm.network "public_network", ip: "192.168.129.199", bridge: "eno2"
  config.vm.box = "ubuntu/focal64"
#  config.vm.network "forwarded_port", guest: 8080, host: 8080
#  config.vm.network "forwarded_port", guest: 8085, host: 8085
#  config.vm.network "forwarded_port", guest: 5000, host: 5000
#  config.vm.network "forwarded_port", guest: 9000, host: 9000


  ## VM Name Ubuntu - com o nome do projeto
  config.vm.define 'ubuntu' do |ubuntu|
      ubuntu.vm.hostname = "ubuntu"
#      ubuntu.vm.network "private_network", ip: "192.168.56.199"  # IP da maquina
      
    
  # Configurações de Size da VM
    ubuntu.vm.provider "virtualbox" do |v|
      v.name = "ubuntu"
      v.memory = 8024
      v.cpus = 4
    end



  # Configura a VM
    ubuntu.vm.provision :ansible do |ansible|
#        ansible.install_mode = "default"
        ansible.playbook = "./ansible/playbook.yml"
        ansible.verbose  = true
#        ansible.install  = true
        ansible.limit    = "all" 
        ansible.inventory_path = "./ansible/inventory.yml"
    end

  end

end
