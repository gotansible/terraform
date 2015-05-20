# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANT_VERSION = 2
Vagrant.configure(VAGRANT_VERSION) do |config|
	config.vm.define "terraform" do |server|
		server.vm.box = "hashicorp/precise64"
		server.vm.hostname = "terraform"
        server.vm.provider "vmware_fusion" do |v|
			v.vmx["memsize"] = "2048"
		end

		server.vm.provision :ansible do |ansible|
			ansible.playbook = "test.yml"
		end
	end
end
