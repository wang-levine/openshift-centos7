Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "master" do |master|
    master.vm.box = "centos/7"
    master.vm.network "public_network"
  end

  config.vm.define "node" do |node|
    node.vm.box = "centos/7"
    node.vm.network "public_network"
  end
end
