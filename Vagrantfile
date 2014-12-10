# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.box = 'hashicorp/precise64'
  config.vm.hostname = 'nodejs'

  config.vm.network 'private_network', ip: '192.168.33.11'

  config.vm.network :forwarded_port, guest: 8000, host: 8000

  # config.vm.synced_folder "../", "/home/vagrant/", type: "nfs", mount_options: ['rw', 'vers=3', 'tcp', 'fsc']

  config.vm.provision :puppet do |puppet|
    puppet.manifests_path = 'puppet/manifests'
    puppet.module_path    = 'puppet/modules'
  end

end
