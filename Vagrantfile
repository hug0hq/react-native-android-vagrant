Vagrant.configure("2") do |config|

  #Box Settings
  config.vm.box = "ubuntu/xenial64"

  #Provider Settings
  config.vm.provider "virtualbox" do |vb|    
    vb.memory = "4096"
    vb.cpus = "1"
    vb.customize ["setextradata", :id, "VBoxInternal2/SharedFoldersEnableSymlinksCreate/v-root", "1"]
    vb.customize ["setextradata", :id, "VBoxInternal2/SharedFoldersEnableSymlinksCreate/vagrant_sync", "1"]
    vb.customize ["modifyvm", :id, "--usb", "on"]
  end

  #Network Settings
  config.vm.network "forwarded_port", guest: 8081, host: 8081

  #Folder Settings
  config.vm.synced_folder ".", "/vagrant"
  config.vm.synced_folder ".", "/home/vagrant/vagrant_sync"
  
  #Provision Settings
  $script = <<-SCRIPT
    apt-get update > /dev/null
    apt-get upgrade -y > /dev/null
  SCRIPT
  config.vm.provision "shell", inline: $script

  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "playbook.yml"
  end

end
