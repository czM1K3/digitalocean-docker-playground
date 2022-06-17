# DigitalOcean Docker playground
Quick way to spin up VM on DigitalOcean with Docker installed

## Requirements
- **Vagrant**
- **Ansible**
- Docker Ansible role (```ansible-galaxy install geerlingguy.docker```)


## Commands
- To start VM
	```bash
	vagrant up
	```
- To SSH to VM
	```bash
	vagrant ssh
	```
- To destroy VM
	```bash
	vagrant destroy
	```

## VM sizes
- s-1vcpu-1gb-amd
- s-1vcpu-2gb-amd
- s-2vcpu-2gb-amd
- s-2vcpu-4gb-amd
- s-4vcpu-8gb-amd