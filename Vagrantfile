Vagrant.configure(2) do |config|
#config cho tất cả các nodes
   config.vm.box = 'generic/rhel9'
   config.vm.provider "virtualbox" do |vb|
      vb.memory = 2048
      vb.cpus = 1
   end

#config control host
   config.vm.define "control" do |control|
      control.vm.hostname = "control"
      control.vm.network :private_network, ip: "192.168.80.100"
      control.vm.provider "virtualbox" do |vb|
         vb.name = "control"
         vb.memory = 512
         vb.cpus = 1
      end
   end 

#config master node
   config.vm.define "k8s-master" do |master|
      master.vm.hostname = "server"
      master.vm.network :private_network, ip: "192.168.80.110"
      master.vm.provider "virtualbox" do |vb|
         vb.name = "server"
         vb.memory = 4096
         vb.cpus = 2
      end
   end 

#config worker node thứ nhất
   config.vm.define "k8s-worker1" do |worker1|
      worker1.vm.hostname = "node-0"
      worker1.vm.network :private_network, ip: "192.168.80.120"
      worker1.vm.provider "virtualbox" do |vb|
         vb.name = "node-0"
      end
   end 

#config worker node thứ hai
   config.vm.define "k8s-worker2" do |worker2|
      worker2.vm.hostname = "node-1"
      worker2.vm.network :private_network, ip: "192.168.80.130"
      worker2.vm.provider "virtualbox" do |vb|
         vb.name = "node-1"
      end
   end
end
