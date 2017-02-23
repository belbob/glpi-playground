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

### Installation glpi-playground

Open a terminal, go to the "my-glpi-playground" directory to store this project and issue the following commands:

create the glpi-vm

```ShellSession
$ vagrant up
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
