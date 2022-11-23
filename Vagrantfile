ENV["VAGRANT_DEFAULT_PROVIDER"] = "virtualbox"

Vagrant.configure("2") do |config|
    config.vm.box = "kalilinux/rolling"

    config.vm.provider "virtualbox" do |vb|
        vb.name = "Kali Linux"
        vb.gui = true
        vb.cpus = 2
        vb.memory = 2048
    end

    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "playbook.yaml"
    end
end
