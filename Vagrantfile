# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  # DSM Vagrant Box

  # Box
  config.vm.box = "dsm_vagrant_box"
  config.vm.box_url = "http://dsm-vagrant-box.s3.amazonaws.com/dsm_vagrant_box.box"

  # Public Network
  config.vm.network "public_network", auto_config: false

  # Shared Folder
  config.vm.synced_folder '.', '/vagrant', disabled: true

  # SSH
  config.ssh.username = "root"
  # config.ssh.password = "vagrant"
  # config.ssh.insert_key = false
  config.ssh.shell = "ash"

  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM
    # vb.memory = "2048"

    # Attach the boot ISO
    vb.customize ["storageattach", :id, "--storagectl", "IDE", "--port", "0", "--device", "0", "--type", "dvddrive", "--medium", "XPEnoboot_DS3615xs_5.1-5022.3.iso"]
  end

end
