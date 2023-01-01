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

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: minikuber, x: 42 }

License
-------

MIT

Author Information
------------------

Loyd Padgett - loydpadgett@gmail.com - github.com/loydpadgett
