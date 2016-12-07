server_script =<<SCRIPT
curl -sSL https://get.docker.com/ | sh
apt-get install -y git-core
sudo usermod -aG docker vagrant
sudo apt-get install python-pip
sudo pip install docker-compose
SCRIPT

Vagrant.configure(2) do |config|

  config.vm.define "docker1" do |docker|
    docker.vm.box = "ubuntu/trusty64"
    docker.vm.network "private_network", ip: "192.168.0.253"
    # docker.vm.hostname = "docker1.vagrant.test"
    docker.vm.provider "virtualbox" do |v|
      v.memory = 4096
      v.cpus = 2
    end
    docker.vm.provision "shell", inline: server_script
  end

end

