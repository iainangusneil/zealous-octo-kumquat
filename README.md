# zealous-octo-kumquat
ansible elasticsearch vagrant.

Inventory:

    * Vagrantfile : Uses jhcook/centos7 box from vagrant cloud as a base. Configures some basic Virtual box setting and ansible provisioning
    * Ansible:
             * elasticsearch_playbook.yml : the playbook to provision the box
             * roles:
                * elasticsearch: Ansible role I wrote to install and run elasticsearch with definable clustername and heapsize
                * ansbilebit.oracle-java: Installed via ansible galaxy (elasticsearch performs best on top of oracles java)
                * ansiblebit.launchpad_ppa_webupd8 : Installed via ansible galaxy as dependancy to oracle-java



Usage:
$ git clone https://github.com/iainangusneil/zealous-octo-kumquat.git

$ cd ./zealous-octo-kumquat

$ vagrant up

$ vagrant provision
