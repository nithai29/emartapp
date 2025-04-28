Vagrant.configure("2") do |config|
  config.hostmanager.enabled = true 
  config.hostmanager.manage_host = true
  config.vm.synced_folder ".", "/vagrant"
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "4096"
  end
### Ubuntu  vm ###
  config.vm.define "ubuntu" do |ubuntu|
    ubuntu.vm.box = "bento/ubuntu-22.04"
    ubuntu.vm.box_version = "202407.23.0"
    ubuntu.vm.hostname = "ubuntu20"
    ubuntu.vm.provision "shell", path: "/Users/nithaikaringula/Downloads/vagrant/linux/docker_install.sh"
    ubuntu.vm.network "private_network", ip: "192.168.56.51"
  end
end
