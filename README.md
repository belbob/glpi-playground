# glpi-playground
This is an Ansible project with a development environment powered by Vagrant, to play with GLPI, fusioninventory, datainjection, and more.

This project sets up:

* 1 virtual machine with centos/7
* MariaDB and phpMyAdmin
* php 7.1
* GLPI and some plugins

This project is intended as a demo/playground for a inventory-introductory , teaching git, vagrant and ansible, in the most simple way, and still useable in my classroom. Surely , this playbook can still be improved, but this way it is manageable in my classroom with my students.

## Dependencies

I use as host a Fedora workstation, make sure you have installed :

- vagrant
- vagrant-libvirt
- vagrant-hostmanager
- ansible (ver. 2+)
- git

## Getting started

When cloning, choose a more suiteable  name for the target directory!

```ShellSession
$ git clone https://github.com/belbob/glpi-playground.git my-glpi-playground
```
After cloning, it's best to remove the `.git` directory and initialise a new repository. The history of the code is most probably irrelevant for your glpi-playground project...

### Installation glpi-playground with Vagrant

Open a terminal, go to the "my-glpi-playground" directory to store this project and issue the following commands:

Edit hosts file and gif a suiteable hostname, only the first hostname will be used by Vagrant.

create the glpi-vm

```ShellSession
$ vagrant up
```

### Installation glpi-playground with ansible-playbook remote

Create a machine with a CentOS/7 - minimal install. Use this IP-address for the hosts file.

Edit hosts file and gif a suiteable hostname and IP-address.

Add id_rsa.pub key for passwordless login.

```ShellSession
$ ssh-copy-id -i ~/.ssh/id_rsa.pub root@192.168.xxx.xxx
```

```ShellSession
$ ansible-playbook -i hosts site.yml
```

### Installation glpi-playground on a local machine

Create a updated machine with a CentOS/7 - minimal install. Use use a fix IP-address.

make sure you have installed dependencies:

```ShellSession
# yum -y install epel-release
# yum -y install git ansible
```
clone glpi-playground

```ShellSession
$ git clone https://github.com/belbob/glpi-playground.git
```
goto glpi-playgroung

```ShellSession
$ cd glpi-playground.git
```
Edit hosts file and change the hostname and IP-address before run:

```ShellSession
ansible-playbook -i hosts -c local site.yml
```

## some issues


## Contributing

Issues, feature requests, ideas are appreciated and can be posted in the Issues section. Pull requests are also very welcome. Preferably, create a topic branch and when submitting, squash your commits into one (with a descriptive message).

## License

Licensed under the "GNU GENERAL PUBLIC LICENSE Version 3, 29 June 2007". See [LICENSE.md](/License.md) for details.

## Author Information

Written by Robert Keersse (robert.keersse@gmail.com)

Contributions by:

-
