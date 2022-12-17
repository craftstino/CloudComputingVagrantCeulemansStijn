$myscript = <<-SCRIPT
sudo apt upgrade -y
sudo  apt update -y
sudo apt-get install sshpass -y
sudo apt install ansible -y
sudo apt install software-properties-common -y
sudo apt-add-repository ppa:ansible/ansible -y
sudo  apt update -y
sudo apt install ansible -y
sudo cp /testing/hosts /etc/ansible/hosts
SCRIPT


Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.define "server1" do |server1|
    server1.vm.box = "ubuntu/trusty64"
    server1.vm.hostname = "server1"
    server1.vm.network "forwarded_port" , guest: 80, host: 4571
    server1.vm.network "private_network" , ip: "10.10.1.2"

  end

  config.vm.define "server2" do |server2|
    server2.vm.box = "ubuntu/trusty64"
    server2.vm.hostname = "server2"
    server2.vm.network "forwarded_port" , guest: 80, host: 4572
    server2.vm.network "private_network" , ip: "10.10.1.3"

  end

  config.vm.define "database" do |database|
    database.vm.box = "ubuntu/trusty64"
    database.vm.hostname = "database"
    database.vm.network "forwarded_port" , guest: 80, host: 4573
    database.vm.network "private_network" , ip: "10.10.1.4"

  end

  config.vm.define "ansible" do |ansible|
    ansible.vm.box = "ubuntu/trusty64"
    ansible.vm.hostname = "ansible"
    ansible.vm.network "private_network" , ip: "10.10.1.5"
    ansible.vm.synced_folder "test-src/", "/testing"
    ansible.vm.provision "shell" , inline: $myscript

  end


end
