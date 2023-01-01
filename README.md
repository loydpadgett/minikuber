Minikuber
=========

A role to install a minikube cluster on a rhel vm. 

Requirements
------------

The requirements are satisfied by the role in the early stages. 
- The kubernetes and openshift modules need to be installed with the --user option. 
- libvirt needs to be installed and enabled
- the user needs to be in the libvirt group. 

Role Variables
--------------

The role variables will mostly be pre-set, the only variables that would affect the cluster would be net driver and memory and cpu size. 

Example Playbook
----------------

This role is using the {{ target }} variable and would need to have the target host specified on the command line. The other variable that will most likely need to be changed is the {{ user }} variable. This variable is located in the defaults/main.yml file. Once changed, the role will correctly populate the needed plays with the user variable.  

    - hosts: "{{ target }}"
      roles:
         - minikuber

License
-------

MIT

Author Information
------------------

Loyd Padgett - loydpadgett@gmail.com - github.com/loydpadgett
