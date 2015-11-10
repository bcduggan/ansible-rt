# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.define :rt do |rt|
    rt.vm.box = "debian/jessie64"
    rt.vm.hostname = "rt"
    rt.vm.network :forwarded_port, guest: 80, host:8080
    rt.vm.provider :virtualbox do |vb|
      vb.name = "rt"
      vb.memory = 1024
    end
    rt.vm.provision "ansible" do |ansible|
      ansible.host_key_checking = false
      ansible.playbook = "./rt.yml"
    end
  end
end
