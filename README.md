Role Name
=========

This role automates the process of adding users to an existing Intersystems Cache installation. The role also allows for the removal of users

Requirements
------------

It is assumed that Cache is already installed on the server.

Role Variables
--------------

instname - The name of the installed instance

[ Default - NONE - Required for both adding and removing users ]

username - The login user name

[ Default - NONE - Required for both adding and removing users ]

password - The password for the user

[ Default - NONE - Required for adding a users ]

fullname - The full name of the user

[ Default - NONE - Required for adding a users ]

namespace - The default namespace for the user

[ Default - NONE - Required for adding a users ]

Rowle - The role assigned to the user

[ Default - NONE - Required for adding a users ]

stayte - Either present to add a user or absent to delete

[ Default - NONE - Required for both adding and deleting users ]

Example Playbook
----------------

Including an example of how to use your role (for instance, with variables passed in as parameters) is always nice for users too:

    - hosts: servers
      role: cache-user
      username: test
      password: tester
      fullname: Tommy Tester
      namespace: TEST
      rowle: %All
      stayte: present


    - hosts: servers
      role: cache-user
      username: test
      stayte: absent


License
-------

BSD

Author Information
------------------

Raman Sailopal
