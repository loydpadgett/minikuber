Minikuber
=========

A role to install a minikube cluster on a rhel vm. 

Requirements
------------

The requirements are satisfied by the role in the early stages. 
- An internet connection is required. 
- specify a named user in the defaults/main.yml file. 
- install libvirt and enable libvirtd
- add user to the libvirt group

Role Variables
--------------

The role variables will mostly be pre-set, please set the "{{ user }}" and "{{ target }}" variables in the defaults/main.yml file or on the command line with the -e option. 

Example Playbook
----------------

This role is using the {{ target }} variable and would need to have the target host specified on the command line. The other variable that will most likely need to be changed is the {{ user }} variable. This variable is located in the defaults/main.yml file. Once changed, the role will correctly populate the needed plays with the user variable.  

    - hosts: "{{ target }}"
      vars: 
        - user: user1
      roles:
         - minikuber

License
-------

MIT

Author Information
------------------

Loyd Padgett - loydpadgett@gmail.com - github.com/loydpadgett
