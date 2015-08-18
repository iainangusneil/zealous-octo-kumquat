# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

	# All Vagrant configuration is done here. The most common configuration
	# options are documented and commented below. For a complete reference,
	# please see the online documentation at vagrantup.com.

	# Every Vagrant virtual environment requires a box to build off of.
	# this is just an appropriate shaped box for demonstrtation purposes
	config.vm.box = "jhcook/centos7"

	config.vm.provider "virtualbox" do |vb|

		# Don't boot with headless mode
		#vb.gui = true
		
		#up cpu and memory because Java
		vb.memory = 2048
		vb.cpus = 2
		
		# turn off usb in virtual box incase it could be handled	
		vb.customize ["modifyvm", :id, "--usb", "off"]
		vb.customize ["modifyvm", :id, "--usbehci", "off"]

	end


	config.vm.provision "ansible" do |ansible|
        ansible.playbook = "./ansible/elasticsearch_playbook.yml"
    end

end
