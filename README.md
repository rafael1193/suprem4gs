# README

SUPREM is an advanced two dimensional process simulator for silicon and
gallium arsenide, originally developed at Stanford University.

Original sources were designed to build on classic UNIX operating systems
and cannot be built on GNU/Linux. 

This repository contains patched source files to allow compilation, without
X11 support, on recent GNU/Linux operating systems.

Actually it builds on:

* Fedora 20 x86-64
* Fedora 20 x86

And it runs on:

* Fedora 20 x86-64
* Ubuntu 13.10 x86-64

If you find other supported operating systems, please, fill an issue with
instructions.

## Instructions

### Fedora

    sudo yum install gcc compat-gcc-34-g77
    make depend install
    ./suprem4gs

## Original README

(C) Copyright (1994) The Board of Trustees of the Leland Stanford Junior
University. Except for commercial resale, lease, license or other commercial
transactions, permission is hereby given to use, copy, modify, and
distribute this software. STANFORD MAKES NO REPRESENTATIONS OR WARRANTIES
OF ANY KIND CONCERNING THIS SOFTWARE.

No support is implied or provided for these older versions of Stanford
TCAD software.

============

Cogenda Pte Ltd provides a series of patches to the SUPREM-IV in the hope
that they are useful. The patches are provided under the same license terms
as the original SUPREM-IV program (quoted above).

Cogenda does not sell SUPREM-IV. If you are seeking a commercial version of
it, please contact a commercial vendor listed in the web page
[ http://www-tcad.stanford.edu/tcad/programs/oldftpable.html ].

We do not intend to add new functionality to SUPREM-IV, since this is a
very old code base.

------------

To compile the SUPREM-IV.GS code and install the files, several changes
to the Makefile may be required.  The Makefile is documented to help
you decide what changes to make where. 

Additional changes may be required to the file src/include/sysdep.h.

Please note that in addition to C a few routines are written in FORTRAN
so you will need a FORTRAN compiler as well as C.

A Bourne shell script called suprem4gs has been included in this
distribution.  I would suggest that the actual program and data
files be stored under a non-system directory available to the
person will be responsible for the program and that the suprem4gs
file be edited to point to that directory.  If suprem4gs is then
placed in a bin directory in most user's PATH (i.e. /usr/local/bin)
updates and modifications become much simpler.

Stephen Hansen
Stanford University
February 4, 1993
