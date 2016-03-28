Ansible Role - gromacs
======================

This playbook installs Gromacs with double precision and MPI support.

Platforms
---------

CentOS 6.7 is the only platform that is supported and tested so far.

Role Variables
--------------

- Check out [defaults/main.yml](defaults/main.yml)

Dependencies
------------

- RDI2.gcc
- RDI2.openmpi
- RDI2.binutils

Installation
------------

Regular installation:

```
ansible-galaxy install RDI2.gromacs
```

Installation to a specific directory(e.g. roles/):

```
ansible-galaxy install -p roles/ RDI2.gromacs
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: RDI2.gromacs }

License
-------

MIT License.

Author Information
------------------

- Koji Tanaka, RDI2
