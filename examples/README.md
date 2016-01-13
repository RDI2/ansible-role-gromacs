Test this playbook with Vagrant
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

The output `gmx_mpi_d --version` should look like this:

```
GROMACS:      gmx_mpi_d, VERSION 5.1.1 (double precision)
Executable:   /opt/gromacs/5.1.1/bin/gmx_mpi_d
Data prefix:  /opt/gromacs/5.1.1
Command line:
  gmx_mpi_d --version

GROMACS version:    VERSION 5.1.1
Precision:          double
Memory model:       64 bit
MPI library:        MPI
OpenMP support:     enabled (GMX_OPENMP_MAX_THREADS = 32)
GPU support:        disabled
OpenCL support:     disabled
invsqrt routine:    gmx_software_invsqrt(x)
SIMD instructions:  AVX_256
FFT library:        fftw-3.3.4-sse2-avx
RDTSCP usage:       enabled
C++11 compilation:  disabled
TNG support:        enabled
Tracing support:    disabled
Built on:           Wed Jan 13 14:59:50 UTC 2016
Built by:           root@localhost.localdomain [CMAKE]
Build OS/arch:      Linux 2.6.32-573.el6.x86_64 x86_64
Build CPU vendor:   GenuineIntel
Build CPU brand:    Intel(R) Core(TM) i5-5257U CPU @ 2.70GHz
Build CPU family:   6   Model: 61   Stepping: 4
Build CPU features: aes apic avx clfsh cmov cx8 cx16 lahf_lm mmx msr nonstop_tsc pclmuldq popcnt pse rdrnd rdtscp sse2 sse3 sse4.1 sse4.2 ssse3
C compiler:         /opt/openmpi/1.10.1/bin/mpicc GNU 4.4.7
C compiler flags:    -mavx    -Wundef -Wextra -Wno-missing-field-initializers -Wno-sign-compare -Wpointer-arith -Wall -Wno-unused -Wunused-value -Wunused-parameter  -O3 -DNDEBUG -funroll-all-loops  -Wno-array-bounds
C++ compiler:       /opt/openmpi/1.10.1/bin/mpicxx GNU 4.4.7
C++ compiler flags:  -mavx    -Wundef -Wextra -Wno-missing-field-initializers -Wpointer-arith -Wall -Wno-unused-function  -O3 -DNDEBUG -funroll-all-loops  -Wno-array-bounds
Boost version:      1.55.0 (internal)
```
