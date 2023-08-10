# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.

Vagrant.configure("2") do |config|
    # config.vm.box = "ubuntu/focal64"
    # config.vm.box = "ubuntu/jammy64"
    


    config.vm.box_check_update = false
    config.ssh.insert_key = false
    # insecure_private_key download from https://github.com/hashicorp/vagrant/blob/master/keys/vagrant
    config.ssh.private_key_path = "insecure_private_key"

    c_machines = {
        'c1'   => '192.168.28.11',
        'c2'   => '192.168.28.12',
        'c3'   => '192.168.28.13',
        'c4'   => '192.168.28.14',
        'c5'   => '192.168.28.15',
        'c6'   => '192.168.28.16',        
                
    }

    c_machines.each do |name, ip|
        config.vm.define name do |machine|
            machine.vm.network "private_network", ip: ip
            machine.vm.hostname = name
            machine.vm.provider :virtualbox do |vb|
                #vb.name = name
                vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
                vb.customize ["modifyvm", :id, "--vram", "32"]
                vb.customize ["modifyvm", :id, "--ioapic", "on"]
                vb.customize ["modifyvm", :id, "--cpus", "2"]
                vb.customize ["modifyvm", :id, "--memory", "2048"]
            end

            if name == "c1"
                machine.vm.box = "ubuntu/focal64"
            end
            if name == "c2"
                machine.vm.box = "ubuntu/jammy64"
            end
            if name == "c3"
                machine.vm.box = "centos/7"
            end
                 

            machine.vm.provision "shell", inline: <<-SHELL
            echo "root:vagrant" | sudo chpasswd
            bash /vagrant/init-os.sh
            SHELL
        end
    end




end