# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  # Disable default sync folder
  config.vm.synced_folder ".", "/home/vagrant/sync", disabled: true
  config.vm.synced_folder ".", "/home/vagrant", disabled: true

  config.vm.box = "centos/7"

  config.vm.provision "ansible" do |ansible|
    ansible.host_key_checking = false
    ansible.verbose = "v"
    ansible.playbook = "init_vagrant.yml"
  end

end

