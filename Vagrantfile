Vagrant.configure("2") do |config|
  config.vm.box = "generic/ubuntu1804"

  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y python3 python3-pip libpq-dev python3-dev
    sudo pip3 install psycopg2
    sudo apt-get install -y python3-django
  SHELL
  
  config.vm.provision "file", source: "./Empty_file.txt", destination: "/home/vagrant/"

end
