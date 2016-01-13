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

- [rdi2sys.openmpi](https://galaxy.ansible.com/detail#/role/6460)

Installation
------------

Regular installation:

```
ansible-galaxy install rdi2sys.gromacs
```

Installation to a specific directory(e.g. roles/):

```
ansible-galaxy install -p roles/ rdi2sys.gromacs
```

Example Playbook
----------------

    - hosts: servers
      roles:
         - { role: rdi2sys.gromacs }

License
-------

MIT License.

Author Information
------------------

- Koji Tanaka, RDI2
