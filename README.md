# ansible-admin-roles

Job Name
------------

### Role user Job
Create a new account on an system
We'll create a user who is able to login with the following attributes:

Requirements
------------

RHEL7 or CentOS7


Role Variables
--------------




Dependencies
------------


Example Playbook Role Usage
----------------


    ---
    - name: Create a login user
     user:
      name: newUser
      password: '???'
      groups: # Empty by default, here we give it some groups
       - sudo
      state: present
      shell: /bin/bash       # Defaults to /bin/bash
      system: no             # Defaults to no
      createhome: yes        # Defaults to yes
      home: /home/newUser  # Defaults to /home/<username>



Testing
----------------
To test the playbook locally, first install the required dependencies locally.

    $ ansible-galaxy install --role-file=./roles/requirements.yml --roles-path=roles --force

    $ ansible-galaxy install -r ./roles/requirements.yml --force
    $ ansible-playbook playbook.yml -i inventory 
License
-------

BSD

Author Information
------------------

An optional section for the role authors to include contact information, or a website (HTML is not allowed).

Contributors
------------


References
-----------
[1] https://serversforhackers.com/c/create-user-in-ansible
