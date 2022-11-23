# autokali

An automatic and repeatable way to set up a ready-to-go Kali Linux instance.

## Requirements

- 30GB+ of free disk space (for the `kalilinux/rolling` box)
- A **hypervisor** (preferrably [VirtualBox](https://www.virtualbox.org/wiki/Downloads))
- **[Vagrant](https://developer.hashicorp.com/vagrant/downloads)**
- (optional) **vagrant-vbguest** plugin for automatic VirtualBox Guest Additions install (`vagrant plugin install vagrant-vbguest`)

## Installation

```bash
git clone https://github.com/molu/autokali
cd autokali
vagrant up --provision
```

The variables used by Ansible during the installation may be customized by editing the files inside `vars` directory.

To control which tools have to be installed, delete existing or add new tool definitions in the `tasks/tools` directory.

The Virtual Machine may be customized by editing the existing options in the `Vagrantfile` file or adding new ones ([Vagrantfile Docs](https://developer.hashicorp.com/vagrant/docs/vagrantfile)).
