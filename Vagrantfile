Vagrant.configure("2") do |config|

 #config.vm.provider "virtualbox" do |v|
  #  v.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
   # v.customize ["modifyvm", :id, "--natdnsproxy1", "on"]
 #end

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.10.100"
  config.hostsupdater.aliases = ["development.local"]


  # sync folder from your OS to VM
  # checking the folder is in home page within the VM
  # below automates downloading all dependencies
  config.vm.synced_folder ".", "/home/vagrant/app"  
  #config.vm.sync_folder "app", "/app"

  # run shell script command from environment folder - creating a file called provision.sh
  # add one line in the vagrant file to link the provision.sh at the same time while vm is being created
  config.vm.provision "shell", path: "environment/provision.sh"
end
