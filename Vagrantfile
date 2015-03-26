# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "Ubuntu14.04"

  config.vm.define :test_env do |test_env|
    test_env.vm.network :private_network, ip: "192.168.33.30"
  end

  config.vm.provider "virtualbox" do |vb|
  #   # Don't boot with headless mode
  #   vb.gui = true
    vb.memory = 2048
  end
=begin
  config.vm.provision "ansible" do |ansible|
    #ansible.inventory_path = "hosts"
    ansible.playbook = "playbooks/main.yml"
    ansible.sudo = true
    ansible.verbose = "-vvvv"
    ansible.limit = 'all'
    ansible.host_key_checking = false
    ansible.extra_vars = {
      node: "test_env",
      user: "vagrant",
      ansible_ssh_user: 'vagrant',
      ansible_connection: 'ssh',
      ansible_ssh_args: '-o ForwardAgent=yes'
    }
  end
=end
end
