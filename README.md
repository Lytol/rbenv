rbenv
=====

Install and configure rbenv and ruby-build, and use rbenv to install one or more versions of Ruby.


Requirements
------------

Requirements will automatically be installed by role.


Role Variables
--------------

* `rbenv_ruby_versions`: You can provide one or more Ruby versions to install. No default.
* `rbenv_ruby_default`: Set a global default Ruby for rbenv. No default.
* `rbenv_user`: The user under which rbenv is installed. Note that rbenv is installed system-wide, so we recommend not changing this. Defaults to `rbenv`.
* `rbenv_root`: The directory where rbenv is installed. Note that rbenv is installed system-wide, so we recommend not changing this. Defaults to `/opt/rbenv`.


Dependencies
------------

* [Ansibles.build-essential](https://galaxy.ansible.com/list#/roles/525)
* [Ansibles.git](https://galaxy.ansible.com/list#/roles/527)


Example Playbook
-------------------------

    - hosts: all
      vars:
        rbenv_ruby_versions:
          - 2.1.2
          - 1.9.3-p484
        rbenv_ruby_default: 2.1.2
      roles:
        - rbenv


License
-------

The MIT License (MIT)

Copyright (c) 2014 Brian Smith <bsmith@swig505.com>

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
