BOX_IMAGE = "centos/7"

Vagrant.configure("2") do |config|
  config.vm.define "server" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
    subconfig.vm.hostname = "chef-server"
    subconfig.vm.network :private_network, ip: "10.0.0.10"
    subconfig.vm.provision "shell", path: "install_chef_server.sh"
  end

  config.vm.define "client" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
    subconfig.vm.hostname = "chef-client"
    subconfig.vm.network :private_network, ip: "10.0.0.20"
  end
end
