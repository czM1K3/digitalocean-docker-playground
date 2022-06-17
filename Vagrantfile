require_relative 'vagrant_credentials.rb'
include Secrets

Vagrant.configure('2') do |config|
	config.vm.define "docker" do |config|
		config.vm.provider :digital_ocean do |provider, override|
			override.ssh.private_key_path = SSHKeyPath
			override.vm.box = 'digital_ocean'
			override.vm.box_url = "https://github.com/devopsgroup-io/vagrant-digitalocean/raw/master/box/digital_ocean.box"
			override.nfs.functional = false
			override.vm.allowed_synced_folder_types = :rsync
			provider.token = DOToken
			provider.ssh_key_name = SSHKeyName
			provider.image = VMOS
			provider.region = VMRegion
			provider.size = VMSize
			provider.backups_enabled = false
			provider.private_networking = false
			provider.ipv6 = false
			provider.monitoring = false
		end
		config.vm.provision "ansible" do |ansible|
			ansible.playbook = "playbook.yml"
		end
	end
end