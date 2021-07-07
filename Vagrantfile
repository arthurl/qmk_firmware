Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-21.04"

  # Create a forwarded port mapping which allows access to a specific port
  # within the machine from a port on the host machine. In the example below,
  # accessing "localhost:8080" will access port 80 on the guest machine.
  # config.vm.network "forwarded_port", guest: 80, host: 8080

  # Create a private network, which allows host-only access to the machine
  # using a specific IP.
  # config.vm.network "private_network", ip: "192.168.33.10"

  # Create a public network, which generally matched to bridged network.
  # Bridged networks make the machine appear as another physical device on
  # your network.
  # config.vm.network "public_network"

  # Share an additional folder to the guest VM. The first argument is
  # the path on the host to the actual folder. The second argument is
  # the path on the guest to mount the folder. And the optional third
  # argument is a set of non-required options.
  config.vm.synced_folder "./", "/qmk_firmware"

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    vb.gui = false

    # Customize the amount of memory on the VM:
    vb.memory = "2048"
  end

  #config.vm.provision "shell", inline: <<-SHELL
  #  add-apt-repository -y ppa:hvr/ghc
  #  apt-get update
  #  # see https://github.com/chef/bento/issues/661#issuecomment-248136601
  #  DEBIAN_FRONTEND=noninteractive apt-get -yq -o Dpkg::Options::="--force-confdef" -o Dpkg::Options::="--force-confold" upgrade
  #  apt-get install -y ghc-8.0.2 cabal-install-1.24
  #  apt-get -y autoremove
  #  echo 'export PATH=$HOME/.cabal/bin:/opt/ghc/bin:$PATH' >> /home/vagrant/.bashrc
  #SHELL
  # config.vm.provision :shell, path: "bootstrap.sh"
end
