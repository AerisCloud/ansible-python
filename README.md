aeriscloud.python
=================

Installs python 2.x on your system, also takes care of installing easy_install, pip and virtualenv, as well as custom python packages.

Role Variables
--------------

* __python_packages__: An array of packages, packages can either be a string (will install latest version) or a dict with name and version
* __python_requirements__: The path to a requirements.txt file

Dependencies
------------

aeriscloud.repos for enabling EPEL on Centos.

Example Playbook
----------------

    - hosts: servers
      roles:
         - role: aeriscloud.python
           python_packages:
           - six  # installs latest version of six
           - { name: humanize, version: 0.5 }
           python_requirements: /app/requirements.txt  # runs pip install -r /app/requirements.txt

License
-------

MIT

