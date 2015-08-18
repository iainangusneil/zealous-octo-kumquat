# zealous-octo-kumquat
<p>Uses Ansible to install elasticsearch on a vagrant box.</p>

<h3>Inventory</h3>
<ul>
    <li> Vagrantfile : Uses jhcook/centos7 box from vagrant cloud as a base. Configures some basic Virtual box setting and ansible provisioning</li>
    <li>Ansible:
        <ul>
            <li> elasticsearch_playbook.yml : the playbook to provision the box</li>
            <li>roles:
                <ul>
                  <li> elasticsearch: Ansible role I wrote to install and run elasticsearch with definable clustername and heapsize </li>
                  <li> ansbilebit.oracle-java: Installed via ansible galaxy (elasticsearch performs best on top of oracles java) </li>
                  <li> ansiblebit.launchpad_ppa_webupd8 : Installed via ansible galaxy as dependancy to oracle-java </li>
                </ul>
             </li>
         </ul>
     </li>
</ul>



<h3>Usage</h3>

<ol>
    <li>
        $ git clone https://github.com/iainangusneil/zealous-octo-kumquat.git
    </li>
    <li>
        $ cd ./zealous-octo-kumquat
    </li>
    <li>
        $ vagrant up
    </li>
    <li>
        $ vagrant provision
    </li>

</ol>