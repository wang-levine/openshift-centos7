$script = <<-SCRIPT
sudo yum check-update
sudo yum -y update
sudo yum -y install epel-release centos-release-openshift-origin36
SCRIPT

Vagrant.configure("2") do |config|

  config.vm.define "master" do |master|
    master.vm.box = "centos/7"
    master.vm.network "public_network"
    master.vm.provision "shell", inline: $script
  end

  config.vm.define "node" do |node|
    node.vm.box = "centos/7"
    node.vm.network "public_network"
    node.vm.provision "shell", inline: $script
  end
end
