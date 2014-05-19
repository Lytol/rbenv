rbenv
=====

Install and configure rbenv and ruby-build, and use rbenv to install one or more versions of Ruby.


Requirements
------------

Requirements will automatically be installed by role.


Role Variables
--------------

* `rbenv_user`: Defaults to the Ansible `remote_user`
* `rbenv_ruby_versions`: You can provide one or more Ruby versions to install. Defaults to empty.
* `rbenv_ruby_default`: Set a global default Ruby for rbenv. Defaults to none.


Dependencies
------------

* [Ansibles.build-essential](https://galaxy.ansible.com/list#/roles/525)
* [Ansibles.git](https://galaxy.ansible.com/list#/roles/527)


Example Playbook
-------------------------

    - hosts: all
      vars:
        rbenv_user: deploy
        rbenv_ruby_versions:
          - 2.1.2
          - 1.9.3-p484
        rbenv_ruby_default: 2.1.2
      roles:
        - rbenv


License
-------

MIT
