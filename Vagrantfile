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
  config.vm.synced_folder "app", "/home/vagrant/app"  
  #config.vm.sync_folder "app", "/app"
end
