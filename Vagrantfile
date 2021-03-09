# CENTOS 7, INSTALLED KERNEL-DEVEL, UPDATED KERNEL, YUM

Vagrant.configure("2") do |config|
#     config.vm.box = "centos/7"
    config.vm.box = "../Documents/docs/BACKUPS/vbox-msn-centos7/msn-centos7"

    config.vm.network "forwarded_port", guest: 80, host: 80
    config.vm.network "private_network", ip: "192.168.88.8"
    config.vm.synced_folder "www", "/www/"
    config.vm.synced_folder "provision", "/provision/"
    config.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
    end


    config.vm.provision "post-provision", type: "shell", after: :all, run: "always", inline: <<-SHELL
        echo '=============================================='
        echo '*           POST PROVISION SCREEN            *'
        echo '=============================================='
        echo ''
        echo ''
        echo 'Good. You can now vagrant ssh'
    SHELL

end

# Muhannad Senan