Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.network "forwarded_port", guest: 8080, host: 8080

  # config.vm.synced_folder "../data", "/vagrant_data"

  config.vm.provider "virtualbox" do |vb|
    vb.name = "docker-jenkins"
    vb.memory = "1024"
  end

  config.vm.provision "shell", path:"docker-jenkins-install.sh"
end
