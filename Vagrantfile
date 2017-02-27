Vagrant.configure("2") do |config|
  config.vm.box = "hashicorp/precise64"
  config.vm.provision "file", source: "env.sh", destination: "~/env.sh"
  config.vm.provision :shell, path: "bootstrap.sh"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.network "forwarded_port", guest: 28015, host: 28015
  config.vm.network "forwarded_port", guest: 9001, host: 9001
end
