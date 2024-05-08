MUSIC V
=================

This repository holds the most up-to-date version of MUSIC V. The
program consists of Fortran source code, which has been curated from
various sources, corrected and modernised for compilation on modern
operating systems. It has been tested under the gfortran compiter.
The code also includes a newly written C-language frontend to facilitate
operation.

Building
------

To build MUSIC V you will need to install a Fortran compiller. The
gfortran compiler, which you can find at
http://gcc.gnu.org/wiki/GFortran, has been tested and the sources
are kept up to date with it. You willl also need CMake and a C
compiler installation.

With these installed,

```
$ mkdir build
$ cmake ..
$ make
```

builds the `music5` program.

Installing
--------

Installation is controlled by the CMake option
`CMAKE_INSTALL_PREFIX`. This is set by default to `/usr/local`.

The command

```
make install
```

will install the software to `${CMAKE_INSTALL_PREFIX}/bin`. Depending
on the local admin permissions might be need to perform installation.


Running
--------

Once isntalled, the command `music5` can be run in the command line:

```
music5 [-p pass] <score> <output_file>
```

where `<score>` is the MUSIC V score file name, and `<output_file>`  is the name of a RIFF-WAVE
file to be written by the program. Individual passes can be optionally run using the `-p [1|2|3]`
option. The `-h` prints a help message to the command-line.





