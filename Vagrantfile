
Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/trusty64"
    config.vm.provider "virtualbox" do |vb|
        vb.memory = 512
        vb.cpus = 1
    end

    config.vm.define "wordpress" do |wordpress|
        wordpress.vm.network "public_network", ip: "192.168.101.86"
        wordpress.vm.network "forwarded_port", guest:8666, host: 8666
        wordpress.vm.synced_folder ".configs", "/home/configs"
    end

    config.vm.define "mysql" do |mysql|
        mysql.vm.network "public_network", ip: "192.168.101.87"
        mysql.vm.network "forwarded_port", guest:8686, host: 8686
        mysql.vm.synced_folder ".configs", "/home/configs"
    end
end
