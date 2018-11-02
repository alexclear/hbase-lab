# -*- mode: ruby -*-
# vi: set ft=ruby :

$HBASE1_IP = "172.16.137.2"
$HBASE2_IP = "172.16.137.3"
$HBASE3_IP = "172.16.137.4"
$HBASE4_IP = "172.16.137.5"
$HBASE5_IP = "172.16.137.6"

ANSIBLE_RAW_SSH_ARGS = []

ANSIBLE_RAW_SSH_ARGS << " -o IdentityFile=./.vagrant/machines/hbase1/virtualbox/private_key "
ANSIBLE_RAW_SSH_ARGS << " -o IdentityFile=./.vagrant/machines/hbase2/virtualbox/private_key "
ANSIBLE_RAW_SSH_ARGS << " -o IdentityFile=./.vagrant/machines/hbase3/virtualbox/private_key "
ANSIBLE_RAW_SSH_ARGS << " -o IdentityFile=./.vagrant/machines/hbase4/virtualbox/private_key "
ANSIBLE_RAW_SSH_ARGS << " -o IdentityFile=./.vagrant/machines/hbase5/virtualbox/private_key "

Vagrant.configure("2") do |config|
  config.vm.define "hbase1" do |hbase1|
    hbase1.vm.box = "ubuntu/bionic64"
    hbase1.vm.hostname = "hbase1"
    hbase1.vm.network "private_network", ip: $HBASE1_IP

    hbase1.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase1.vm.provision "shell", inline: "apt-get install -y python"
  end

  config.vm.define "hbase2" do |hbase2|
    hbase2.vm.box = "ubuntu/bionic64"
    hbase2.vm.hostname = "hbase2"
    hbase2.vm.network "private_network", ip: $HBASE2_IP

    hbase2.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase2.vm.provision "shell", inline: "apt-get install -y python"
  end

  config.vm.define "hbase3" do |hbase3|
    hbase3.vm.box = "ubuntu/bionic64"
    hbase3.vm.hostname = "hbase3"
    hbase3.vm.network "private_network", ip: $HBASE3_IP

    hbase3.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase3.vm.provision "shell", inline: "apt-get install -y python"
  end

  config.vm.define "hbase4" do |hbase4|
    hbase4.vm.box = "ubuntu/bionic64"
    hbase4.vm.hostname = "hbase4"
    hbase4.vm.network "private_network", ip: $HBASE4_IP

    hbase4.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase4.vm.provision "shell", inline: "apt-get install -y python"
  end

  config.vm.define "hbase5" do |hbase5|
    hbase5.vm.box = "ubuntu/bionic64"
    hbase5.vm.hostname = "hbase5"
    hbase5.vm.network "private_network", ip: $HBASE5_IP

    hbase5.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase5.vm.provision "shell", inline: "apt-get install -y python"
    hbase5.vm.provision "ansible" do |ansible|
      ansible.playbook = "ansible/site.yml"
      ansible.inventory_path = "ansible/inventory"
      ansible.become = true
      ansible.limit = "all"
      ansible.raw_ssh_args = ANSIBLE_RAW_SSH_ARGS
    end
  end
end
