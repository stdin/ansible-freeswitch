Vagrant.configure(2) do |config|
  config.vm.box = "debian/jessie64"

  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "vagrant_playbook.yml"
  end
end
