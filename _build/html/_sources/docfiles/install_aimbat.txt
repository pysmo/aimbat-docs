=================
Installing AIMBAT
=================

.. ############################################################################ ..
.. #                          GETTING THE PACKAGES                            # ..
.. ############################################################################ ..

Getting the Packages
--------------------

AIMBAT is released as a sub-package of pysmo in the name of ``pysmo.aimbat`` along with another sub-package ``pysmo.sac``. The latest stable release of AIMBAT is available for download at the `official project webpage <http://www.earth.northwestern.edu/~xlou/aimbat.html>`_. 

We are working on a new release of AIMBAT, available on `Github <https://github.com/pysmo>`_. We are adding more features to make using AIMBAT more convenient, and fixing some bugs in the old code. Download `pysmo.aimbat <https://github.com/pysmo/aimbat>`_ and `pysmo.sac <https://github.com/pysmo/sac>`_ from Github. You will now have two folders called ``aimbat`` and ``sac`` respectively.

You may want to download `example code <https://github.com/pysmo/data-example>`_ to run AIMBAT on, as well. 

.. ############################################################################ ..
.. #                          GETTING THE PACKAGES                            # ..
.. ############################################################################ ..





.. ############################################################################ ..
.. #                        WHERE TO INSTALL THE PACKAGES                     # ..
.. ############################################################################ ..

Where to install the packages
-----------------------------

There are several options to install the packages. If you just want to use AIMBAT, it is best to store it somewhere where you would not touch the packages so easily, such as the Python ``site-packages`` directory. If you would like to make some changes to the Python code, it is best to store it somewhere pretty accessible, such as your ``home`` directory on your computer, or in ``Documents``.

Installing into the Python Site-Packages Directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

To find out where the Python Site-Packages Directory is, in the python console, do::

	import site;
	site.getsitepackages()

Whatever is output is obtained, lets call it ``<pkg-install-dir>``. Make a directory called ``pysmo``, and place the sac and aimbat directories inside ``<pkg-install-dir>/pysmo``.

Installing into the home directory
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Open your terminal. Type ``open .`` and that will open your home directory. Transfer the ``aimbat`` and ``sac`` repositories inside there. 

.. ############################################################################ ..
.. #                        WHERE TO INSTALL THE PACKAGES                     # ..
.. ############################################################################ ..







.. ############################################################################ ..
.. #                             BUILDING PYSMO                               # ..
.. ############################################################################ ..

Building the Pysmo Packages
---------------------------

You need to be an administrator on the computer you are installing AIMBAT in, as you need to run the commands with ``sudo``.

Building pysmo.sac
~~~~~~~~~~~~~~~~~~

Python module ``Distutils`` is used to write a setup.py script to build, distribute, and install ``pysmo.sac``. cd into the ``sac`` directory on the command line and run::

	sudo python setup.py build
  	sudo python setup.py install

.. image::install-aimbat-images/site_package_location.png

If you successfully installed the sac module, in the python console, this should happen after you type :code:`from pysmo import sac`

.. image::install-aimbat-images/sac_installed.png

Installing pysmo.aimbat
~~~~~~~~~~~~~~~~~~~~~~~

Three sub-directories are included in the ``aimbat`` directory
* ``example``: Example SAC files
* ``scripts``: Python scripts to run at the command line
* ``src``: Python modules to install

The core cross-correlation functions are written in both Python/Numpy (``xcorr.py``) and Fortran (``xcorr.f90``). Therefore, we need to use Numpy’s ``Distutils`` module for enhanced support of Fortran extension. The usage is similar to the standard Disutils.

Note that some sort of Fortran compiler must already be installed first. Specify them in place of gfortran in the following commands.

cd into the directory the ``aimbat`` package was placed in, and type::

	sudo python setup.py build --fcompiler=gfortran
  	sudo python setup.py install

to install the :code:`src` directory.

Add ``<path-to-folder>/aimbat/scripts`` to environment variable ``PATH`` in a shells start-up file for command line execution of the scripts. Inside the :code:`.bashrc` file, add the lines

Bash Shell Users::
	
	export PATH=$PATH:<path-to-folder>/aimbat/scripts 
	export PATH=$PATH:<path-to-folder>/aimbat/additional-processing-scripts

C Shell Users:
	
	setenv PATH=$PATH:<path-to-folder>/aimbat/scripts
	setenv PATH=$PATH:<path-to-folder>/aimbat/additional-processing-scripts


If AIMBAT has beenn installed, type ``from pysmo import aimbat`` in a Python shell, and no errors should appear.

If you have added the scripts right, typing part of the name of the script in the terminal should be sufficient to allow the system autocomplete the name. 


.. ############################################################################ ..
.. #                             BUILDING PYSMO                               # ..
.. ############################################################################ ..

















