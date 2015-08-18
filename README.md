# zealous-octo-kumquat
uses Ansible to install elasticsearch on a vagrant box.


<ul>Inventory :
    <li> Vagrantfile : Uses jhcook/centos7 box from vagrant cloud as a base. Configures some basic Virtual box setting and ansible provisioning</li>
    <li>
        <ul> Ansible:
            <li> elasticsearch_playbook.yml : the playbook to provision the box</li>
            <li>
                <ul>roles:
                  <li> elasticsearch: Ansible role I wrote to install and run elasticsearch with definable clustername and heapsize</li>
                  <li> ansbilebit.oracle-java: Installed via ansible galaxy (elasticsearch performs best on top of oracles java)</li>
                  <li> ansiblebit.launchpad_ppa_webupd8 : Installed via ansible galaxy as dependancy to oracle-java</li>
                </ul>
             </li>
         </ul>
     </li>
 </ul>





Usage:
$ git clone https://github.com/iainangusneil/zealous-octo-kumquat.git

$ cd ./zealous-octo-kumquat

$ vagrant up

$ vagrant provision
