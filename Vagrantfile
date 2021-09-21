Vagrant.configure("2") do |config|
  #config.hostmanager.enabled = true
  #config.hostmanager.manage_host = true
  #config.hostmanager.manage_guest = true
  #config.hostmanager.ignore_private_ip = false
  #config.hostmanager.include_offline = true
#

  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-20.04"
    master.vm.hostname = "master.ravi.local"
    master.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    master.vm.network :forwarded_port, guest: 22, host: 2230, auto_correct: true
#    master.vm.network "private_network", ip: "192.168.101.155"
    #master.vm.synced_folder ".", "/vagrant", type: 'sshfs', create:true 
    #master.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "master_kube.yml"
    #end

  end

  config.vm.define "node1" do |node1|
    node1.vm.box = "bento/ubuntu-20.04"
    node1.vm.hostname = "node1.ravi.local"
    node1.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    node1.vm.network :forwarded_port, guest: 22, host: 2231, auto_correct: true
#    node1.vm.network "private_network", ip: "192.168.101.156"
    #node1.vm.synced_folder ".", "/vagrant", type: 'sshfs', create:true 
    #node1.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "node_kube.yml"
    #end
  end

  config.vm.define "node2" do |node2|
    node2.vm.box = "bento/ubuntu-20.04"
    node2.vm.hostname = "node2.ravi.local"
    node2.vm.network :forwarded_port, guest: 22, host: 2222, id: "ssh", disabled: true
    node2.vm.network :forwarded_port, guest: 22, host: 2232, auto_correct: true
#    node2.vm.network "private_network", ip: "192.168.101.157"
#    node2.vm.memory = 4000
#    node2.vm.cpus = 4000
    #node2.vm.synced_folder ".", "/vagrant", type: 'sshfs', create:true 
    #node2.vm.provision "ansible" do |ansible|
    #  ansible.playbook = "node_kube.yml"
    #end
  end


  config.vm.provider "parallels" do |v|
    v.memory = 4000
    v.cpus = 2
  end
end
