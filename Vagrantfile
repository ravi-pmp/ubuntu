Vagrant.configure("2") do |config|
  #config.hostmanager.enabled = true
  #config.hostmanager.manage_host = true
  #config.hostmanager.manage_guest = true
  #config.hostmanager.ignore_private_ip = false
  #config.hostmanager.include_offline = true


  config.vm.define "master" do |master|
    master.vm.box = "bento/ubuntu-20.04"
    master.vm.hostname = "master.ravi.local"
  end

  config.vm.define "node1" do |node1|
    node1.vm.box = "bento/ubuntu-20.04"
    node1.vm.hostname = "node1.ravi.local"
  end

  config.vm.define "node2" do |node2|
    node2.vm.box = "bento/ubuntu-20.04"
    node2.vm.hostname = "node2.ravi.local"
  end


  config.vm.provider "parallels" do |v|
    v.memory = 4000
    v.cpus = 2
  end
end
