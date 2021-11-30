# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.hostmanager.enabled = true
  config.hostmanager.manage_host = false
  config.hostmanager.manage_guest = true
  config.hostmanager.ignore_private_ip = false
  config.hostmanager.include_offline = true

  config.vm.define "hbase1" do |hbase1|
    hbase1.vm.box = "generic/ubuntu1804"
    hbase1.vm.hostname = "hbase1"

    hbase1.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase1.vm.provider :libvirt do |v, override|
      v.cpu_mode = 'custom'
      v.cpu_model = 'kvm64'
      v.cpus = 4
      v.memory = 8192
    end

    hbase1.vm.provider :hyperv do |v, override|
      hbase1.vm.network "public_network", bridge: "Default Switch"
      v.cpus = 4
      v.memory = 8192
      v.maxmemory = 8192
    end

    hbase1.vm.provision "shell", inline: "apt-get install -y python"
    hbase1.vm.provision "shell", inline: "sed -i -e '/127\.0\.2/d' /etc/hosts"
    hbase1.vm.provision "shell", inline: "sysctl net.ipv6.conf.all.disable_ipv6=1"
    hbase1.vm.provision "shell", inline: "sysctl net.ipv6.conf.default.disable_ipv6=1"
  end

  config.vm.define "hbase2" do |hbase2|
    hbase2.vm.box = "generic/ubuntu1804"
    hbase2.vm.hostname = "hbase2"

    hbase2.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase2.vm.provider :libvirt do |v, override|
      v.cpu_mode = 'custom'
      v.cpu_model = 'kvm64'
      v.cpus = 4
      v.memory = 8192
    end

    hbase2.vm.provider :hyperv do |v, override|
      hbase2.vm.network "public_network", bridge: "Default Switch"
      v.cpus = 4
      v.memory = 8192
      v.maxmemory = 8192
    end

    hbase2.vm.provision "shell", inline: "apt-get install -y python"
    hbase2.vm.provision "shell", inline: "sed -i -e '/127\.0\.2/d' /etc/hosts"
    hbase2.vm.provision "shell", inline: "sysctl net.ipv6.conf.all.disable_ipv6=1"
    hbase2.vm.provision "shell", inline: "sysctl net.ipv6.conf.default.disable_ipv6=1"
  end

  config.vm.define "hbase3" do |hbase3|
    hbase3.vm.box = "generic/ubuntu1804"
    hbase3.vm.hostname = "hbase3"

    hbase3.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase3.vm.provider :libvirt do |v, override|
      v.cpu_mode = 'custom'
      v.cpu_model = 'kvm64'
      v.cpus = 4
      v.memory = 8192
    end

    hbase3.vm.provider :hyperv do |v, override|
      hbase3.vm.network "public_network", bridge: "Default Switch"
      v.cpus = 4
      v.memory = 8192
      v.maxmemory = 8192
    end

    hbase3.vm.provision "shell", inline: "apt-get install -y python"
    hbase3.vm.provision "shell", inline: "sed -i -e '/127\.0\.2/d' /etc/hosts"
    hbase3.vm.provision "shell", inline: "sysctl net.ipv6.conf.all.disable_ipv6=1"
    hbase3.vm.provision "shell", inline: "sysctl net.ipv6.conf.default.disable_ipv6=1"
  end

  config.vm.define "hbase4" do |hbase4|
    hbase4.vm.box = "generic/ubuntu1804"
    hbase4.vm.hostname = "hbase4"

    hbase4.vm.provider :virtualbox do |v, override|
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase4.vm.provider :libvirt do |v, override|
      v.cpu_mode = 'custom'
      v.cpu_model = 'kvm64'
      v.cpus = 4
      v.memory = 8192
    end

    hbase4.vm.provider :hyperv do |v, override|
      hbase4.vm.network "public_network", bridge: "Default Switch"
      v.cpus = 4
      v.memory = 8192
      v.maxmemory = 8192
    end

    hbase4.vm.provision "shell", inline: "apt-get install -y python"
    hbase4.vm.provision "shell", inline: "sed -i -e '/127\.0\.2/d' /etc/hosts"
    hbase4.vm.provision "shell", inline: "sysctl net.ipv6.conf.all.disable_ipv6=1"
    hbase4.vm.provision "shell", inline: "sysctl net.ipv6.conf.default.disable_ipv6=1"
  end

  config.vm.define "hbase5" do |hbase5|
    hbase5.vm.box = "generic/ubuntu1804"
    hbase5.vm.hostname = "hbase5"

    hbase5.vm.provider :virtualbox do |v, override|
      override.vm.synced_folder ".", "/vagrant"
      v.gui = false
      v.customize ["modifyvm", :id, "--cpus", 4]
      v.customize ["modifyvm", :id, "--memory", 8192]
      v.customize ["modifyvm", :id, "--cableconnected1", "on"]
      v.customize ["modifyvm", :id, "--cableconnected2", "on"]
    end

    hbase5.vm.provider :libvirt do |v, override|
      v.cpu_mode = 'custom'
      v.cpu_model = 'kvm64'
      v.cpus = 4
      v.memory = 8192
    end

    hbase5.vm.provider :hyperv do |v, override|
      hbase5.vm.network "public_network", bridge: "Default Switch"
      override.vm.synced_folder ".", "/vagrant", type: "smb", smb_username: ENV["SMB_USERNAME"], smb_password: ENV["SMB_PASSWORD"]
      v.cpus = 4
      v.memory = 8192
      v.maxmemory = 8192
    end

    hbase5.vm.provision "shell", inline: "apt-get install -y python"
    hbase5.vm.provision "shell", inline: "sed -i -e '/127\.0\.2/d' /etc/hosts"
    hbase5.vm.provision "shell", inline: "sysctl net.ipv6.conf.all.disable_ipv6=1"
    hbase5.vm.provision "shell", inline: "sysctl net.ipv6.conf.default.disable_ipv6=1"
    hbase5.vm.provision "shell", inline: "cp /vagrant/.vagrant/machines/hbase1/hyperv/private_key /home/vagrant/private_key_hbase1 && cp /vagrant/.vagrant/machines/hbase2/hyperv/private_key /home/vagrant/private_key_hbase2 && cp /vagrant/.vagrant/machines/hbase3/hyperv/private_key /home/vagrant/private_key_hbase3 && cp /vagrant/.vagrant/machines/hbase4/hyperv/private_key /home/vagrant/private_key_hbase4 && cp /vagrant/.vagrant/machines/hbase5/hyperv/private_key /home/vagrant/private_key_hbase5 && chmod 600 /home/vagrant/private_key* && chown vagrant:vagrant /home/vagrant/private_key* && ls -alF /home/vagrant/private_key*"
    hbase5.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible/site.yml"
      ansible.config_file = "ansible/ansible.cfg"
      ansible.inventory_path = "ansible/inventory"
      ansible.become = true
      ansible.galaxy_role_file = "ansible/roles/requirements.yml"
      ansible.galaxy_roles_path = "/etc/ansible/roles"
      ansible.galaxy_command = "sudo ansible-galaxy install --role-file=%{role_file} --roles-path=%{roles_path} --force"
      ansible.limit = "all"
    end
  end
end
