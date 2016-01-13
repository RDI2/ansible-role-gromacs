Tests role gromacs with Vagrant
===============================

Install dependencies:

```bash
ansible-galaxy install -p roles/ -r requirement.yml
```

Vagrant up:

```bash
vagrant up
```

Try gromacs:

```bash
vagrant ssh
export PATH=/opt/gromacs/5.1.1/bin
export LD_LIBRARY_PATH=/opt/gromacs/5.1.1/lib64:$LD_LIBRARY_PATH
gmx_mpi_d --version
```
