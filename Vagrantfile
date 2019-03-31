# $script = <<SCRIPT

# # nodejs
# apt-get -y install g++ git git-core nodejs npm
# npm install n -g
# n stable
# node -v

# SCRIPT 

Vagrant.configure("2") do |config|

  # Box settings
  config.vm.box = "ubuntu/trusty64"

  # Provider Settings
  config.vm.provider "virtualbox" do |vb|
      vb.memory = 1024
      vb.cpus   = 2
  end    

  # Network Settings
  config.vm.network :private_network, ip: "192.168.33.10"
  
  
  # Use :ansible or :ansible_local to
  # select the provisioner of your choice
  config.vm.provision :ansible do |ansible|
    ansible.playbook = "playbook.yml"
  end
  


  # Folder Settings
  config.vm.synced_folder ".", "/vagrant"



  # Provision settings
  #config.vm.provision :shell, :inline => $script
  
end    