Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-19.10"
  config.vm.box_version = "201910.31.0"
  config.vm.provision :shell, path: "bootstrap.sh"

  config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     vb.gui = true
     vb.memory = "4096"
     vb.customize ["modifyvm", :id, "--graphicscontroller", "vboxvga"]
  end
end
