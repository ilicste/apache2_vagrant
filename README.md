# apache2_vagrant
cd to devops/vagrant
mkdir apache 2
cd apache 2
vagrant init -m -f
nano VAGRANTFILE and paste:
Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.network "forwarded_port", guest:80, host:8080, auto_correct: true
  config.vm.synced_folder ".", "/var/www/html"  
 config.vm.provider "virtualbox" do |vb|
  vb.memory = "2048"  
 end
  config.vm.provision "shell", inline: <<-SHELL 
    sudo apt-get update
    sudo apt-get install apache2 -y
    sudo apt-get install mysql-server -y
    sudo apt-get install php5-mysql -y
  SHELL
enda
ctrl+X -> y -> enter
vagrant up
