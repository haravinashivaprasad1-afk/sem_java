Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/jammy64"

  config.vm.define "manager" do |manager|
    manager.vm.hostname = "manager"
    manager.vm.network "private_network", ip: "192.168.56.10"

    manager.vm.network "forwarded_port", guest: 8080, host: 8080

    manager.vm.provider "virtualbox" do |vb|
      vb.memory = 512
      vb.cpus = 1
    end
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.hostname = "worker1"
    worker1.vm.network "private_network", ip: "192.168.56.11"

    worker1.vm.network "forwarded_port", guest: 8080, host: 8081

    worker1.vm.provider "virtualbox" do |vb|
      vb.memory = 384
      vb.cpus = 1
    end
  end

end
