Vagrant.configure("2") do |config|
  # The most common configuration options are documented and commented below.
  # For a complete reference, please see the online documentation at
  # https://docs.vagrantup.com.

  # Every Vagrant development environment requires a box. You can search for
  # boxes at https://vagrantcloud.com/search.
  config.vm.box = "ubuntu/bionic64"
  config.vm.provider "virtualbox" do |vb|
   vb.memory = "2048"
   vb.cpus = 2
  end
  $playbook =  <<-SHELL
   sudo apt update && sudo apt install -y ansible git
   git clone https://github.com/lorisegault/R511.git
   cd R511
   ansible-playbook global.yaml -i "localhost"
  SHELL
  config.vm.provision "shell", inline: $playbook
  end
