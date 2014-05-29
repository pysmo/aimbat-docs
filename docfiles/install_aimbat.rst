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
.. #                          BUILDING PYSMO.SAC                            # ..
.. ############################################################################ ..

Building pysmo.sac
--------------------

Python module :code:`Distutils` is used to write a setup.py script to build, distribute, and install ``pysmo.sac``. In the directory :code:`<pkg-install-dir>/pysmo-sac-0.5>`, type::

	sudo python setup.py build
  	sudo python setup.py install

to install it and its package information file :code:`pysmo.sac-0.5-py2.7.egg-info` to the global site-packages directory :code:`<prefix>/lib/python2.7/site-packages`, which is the same as Numpy, Scipy, and Matplotlib.

.. image::install-aimbat-images/site_package_location.png

If you don’t have write permission to the global site-packages directory, use the `--user` option to install to `<userbase>/lib/python2.7/site-packages`::

	python setup.py install --user

This will install it to your home directory only, not for all users on the computer. Try not to use this option though, as installing without the :code:`sudo` command has caused problems in the past.

If you successfully installed the sac module, in the python console, this should happen after you type :code:`from pysmo import sac`

.. image::install-aimbat-images/sac_installed.png

.. ############################################################################ ..
.. #                          INSTALLING PYSMO.SAC                            # ..
.. ############################################################################ ..





.. ############################################################################ ..
.. #                        INSTALLING PYSMO.AIMBAT                           # ..
.. ############################################################################ ..

Installing pysmo.aimbat
-----------------------

Three sub-directories are included in the :code:`<pkg-install-dir>/pysmo/pysmo-aimbat-0.1.2>` directory: :code:`example`, :code:`scripts`, and :code:`src`, which contain example SAC files, Python scripts to run at the command line, and Python modules to install, respectively.

The core cross-correlation functions in :code:`pysmo.aimbat` are written in both Python/Numpy (:code:`xcorr.py`) and Fortran (:code:`xcorr.f90`). Therefore, we need to use Numpy’s :code:`Distutils` module for enhanced support of Fortran extension. The usage is similar to the standard Disutils.

Note that some sort of Fortran compiler must already be installed first. Specify them in place of gfortran in the following commands.

In the directory :code:`<pkg-install-dir>/pysmo/pysmo-aimbat-0.1.2`, type::

	sudo python setup.py build --fcompiler=gfortran
  	sudo python setup.py install

to install the :code:`src` directory.

Add :code:`<pkg-install-dir>/pysmo/pysmo-aimbat.0.1.2/scripts` to environment variable :code:`PATH` in a shells start-up file for command line execution of the scripts.

Bash Shell Users:
	:code:`export PATH=$PATH:<pkg-install-dir>/pysmo/pysmo-aimbat-0.1.2/scripts` in :code:`.bashrc` files.

C Shell Users:
	:code:`setenv PATH=$PATH:<pkg-install-dir>/pysmo/pysmo-aimbat-0.1.2/scripts` in :code:`.bashrc` files.

If AIMBAT has beenn installed, type from :code:`pysmo import aimbat` in a Python shell, and no errors should appear.


.. ############################################################################ ..
.. #                        INSTALLING PYSMO.AIMBAT                           # ..
.. ############################################################################ ..















