$script1 = <<-SCRIPT
echo '10.0.0.100       haproxy1   haproxy1' >> /etc/hosts
echo '10.0.0.101       web1       web1' >> /etc/hosts
echo '10.0.0.102       web2       web2' >> /etc/hosts
sudo apt-get update -y
sudo apt install nginx -y
sudo systemctl enable nginx
sudo systemctl start nginx
SCRIPT

$script2 = <<-SCRIPT
echo '10.0.0.100       haproxy1   haproxy1' >> /etc/hosts
echo '10.0.0.101       web1       web1' >> /etc/hosts
echo '10.0.0.102       web2       web2' >> /etc/hosts
sudo apt-get update -y
sudo apt-get install software-properties-common -y
sudo add-apt-repository ppa:vbernat/haproxy-1.8 -y
sudo apt-get update -y
sudo apt-get install haproxy=1.8.\* -y
sudo systemctl enable haproxy
sudo systemctl start haproxy
SCRIPT

Vagrant.configure("2") do |config|
  config.vm.define "haproxyserver" do |haproxyserver|
    haproxyserver.vm.box = "ubuntu/xenial64"
    haproxyserver.vm.hostname = "haproxy1"
    haproxyserver.vm.network "private_network", ip: "10.0.0.100"
    haproxyserver.vm.provider "virtualbox" do |v|
      v.name = "haproxy1"
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 1]
      v.customize ["modifyvm", :id, "--name", "haproxy1"]
    end
    haproxyserver.vm.provision "shell", inline: $script2
  end

  config.vm.define "web1" do |web1|
    web1.vm.box = "ubuntu/xenial64"
    web1.vm.hostname = "web1"
    web1.vm.network "private_network", ip: "10.0.0.101"
    web1.vm.provider "virtualbox" do |v|
      v.name = "web1"
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 1]
      v.customize ["modifyvm", :id, "--name", "web1"]
    end
    web1.vm.provision "shell", inline: $script1
  end

  config.vm.define "web2" do |web2|
    web2.vm.box = "ubuntu/xenial64"
    web2.vm.hostname = "web2"
    web2.vm.network "private_network", ip: "10.0.0.102"
    web2.vm.provider "virtualbox" do |v|
      v.name = "web2"
      v.customize ["modifyvm", :id, "--memory", 1024]
      v.customize ["modifyvm", :id, "--cpus", 1]
      v.customize ["modifyvm", :id, "--name", "web2"]
    end
    web2.vm.provision "shell", inline: $script1
  end
end
