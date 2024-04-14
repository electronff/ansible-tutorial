System Inventory
=========

This roles gather system information about networking, utilization and users information


Requirements
------------

ensure that ansible is installed

Role Variables
--------------

Dependencies
------------

Example Playbook
----------------

---
- name: inventory collections
  hosts: all
  become: yes
  become_user: root
  gather_facts: yes
  vars_files:
    - vars/main.yaml
  roles:
    - ping
    - networking
    - utilization
    - users

Command to run the playbook
---------------------------


ansible-playbook  -i inventory/main.yaml  playbook.yaml --ask-become-pass 


Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      roles:
         - { role: username.rolename, x: 42 }

License
-------
devopclinics


