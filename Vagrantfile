Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-19.10"
  config.vm.box_version = "201910.31.0"

  config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     vb.gui = true
     vb.memory = "4096"
     vb.customize ["modifyvm", :id, "--graphicscontroller", "vboxvga"]
  end

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get upgrade -y

    sudo localectl set-keymap dk
    sudo apt-get install --no-install-recommends lubuntu-desktop -y

    sudo apt-get install -y git
    sudo apt-get install -y wget
  SHELL

  config.vbguest.auto_update = true
end
