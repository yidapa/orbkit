.. _installation-instructions:

Installation
============

In this section, we present the manual installation of orbkit on a Unix-like
system.

.. attention::
       
    If you use Windows or Python 3.x, please refer to the Cython version of orbkit: 

      https://github.com/orbkit/orbkit/tree/cython

.. contents:: Table of Contents:
  :local:
  :depth: 2

Prerequisites
-------------

For a proper execution of orbkit, the following Python modules are
required:

1) Python_ 2.6 - 2.7
2) SciPy_ Library of algorithms and mathematical tools
3) NumPy_ Library of high-level mathematical functions
4) h5py_ Interface to the HDF5 binary data format
5) mayavi_ Tool for 3D scientific data visualization (optional)

The package h5py is not mandatory but strongly recommended.

.. _Python: http://www.python.org
.. _SciPy: http://www.scipy.org/
.. _NumPy: http://www.numpy.org/
.. _h5py: http://www.h5py.org/
.. _mayavi: http://docs.enthought.com/mayavi/mayavi/index.html

Instructions
------------

The manual installation of orbkit is a simple procedure and can 
be carried out using ``bash`` as follows:

Choose the directory, where you want to install orbkit. Open a terminal window, 
e.g. ``gnome-terminal``, and navigate to this directory. In this example, we 
will use the home directory. If you want to use a different directory simply replace 
``$HOME`` by your preferred folder throughout the whole section.

    .. code-block:: bash

        $ cd $HOME

Get a copy of orbkit, either with `git`_ or using a `tarball`_. It is strongly
recommended to use `git`_, since this version always contains the newest 
bug fixes and features. If git is not available on your system, the newest 
version can additionally be cloned from https://github.com/orbkit/orbkit. 

  .. _git:

  * Using **git**:

    Clone the repository:

    .. code-block:: bash

        $ git clone https://github.com/orbkit/orbkit.git

  .. _tarball:

  * Using a **tarball**:

    Download the latest orbkit release and extract the file:

    .. code-block:: bash

        $ wget https://github.com/orbkit/orbkit/archive/master.zip
        $ unzip orbkit-master.zip
        $ mv orbkit-master orbkit

In order to use orbkit, you have to add the orbkit directory to your ``PYTHONPATH``
environment variable either temporarily by typing

.. code-block:: bash

    $ export ORBKITPATH=$HOME/orbkit
    $ export PYTHONPATH=$PYHONPATH:$ORBKITPATH

or permanently by adding these lines to your ~/.bashrc file.

To use orbkit as a standalone program, you have to modify your 
``PATH`` variable in the same way:

.. code-block:: bash

    $ export ORBKITPATH=$HOME/orbkit
    $ export PATH=$PATH:$ORBKITPATH/tools

orbkit has been properly tested on Linux, but should also work on other systems.
