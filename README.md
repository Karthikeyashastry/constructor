(conda) constructor
===================

constructor is a tool which allows constructing an installer for
a collection of conda packages.  Basically, it creates an Anaconda-like
installer consisting of conda packages.   This tool was previously
proprietary and known as cas-installer.


Installation:
-------------

It is important that the `constructor` package is installed into the `root`
conda environment (not to be confused with root user).
The following command ensures that this happens:

    $ conda install -n root constructor

Once installed, the constructor command will be available:

    $ constructor -h


Usage:
------

The `constructor` command takes an installer specification directory as its
argument.  This directory needs to contain a file `construct.yaml`,
which specifies the name of the installer, the conda channels to
pull packages from, the conda packages included in the installer etc. .
The complete list of keys in this file can be
found in <a href="./CONSTRUCT.md">CONSTRUCT.md</a>.
Also, the directory may contain some additional optional files (such as a
license file, and image files for the Windows installer).
An example is located
in <a href="./examples/maxiconda">examples/maxiconda</a>.
