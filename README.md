# MPI Mock library

This library is an extension of the custom mpi wrapper introduced
for the compilation of POT3D with LFortran.

This extension was developed as part of an attempt to compile eCLM with LFortran.

If you have activated a conda environment with openmpi and lfortran installed
you should be able to compile this wrapper via:

```sh
gcc -I$CONDA_PREFIX/include -c mpi_wrapper.c
lfortran -c mpi_c_bindings.f90
lfortran -c mpi.f90
```

Aftewards, ensure that the build artifacts are located on the necessary include
path for your application.
