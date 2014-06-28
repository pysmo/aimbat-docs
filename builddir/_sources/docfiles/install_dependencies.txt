==============================
Installing Python Dependencies
==============================

Usually, Macs already have python installed by default. To check if you have python on your mac, open up terminal, and do python in the terminal. If python is installed you should see a python console show up, displaying the version number of python. The version number should be at least 2.7 or higher. If python is not installed, you should see an error message show up. However, you may or may not have some necessary packages installed. 



.. ############################################################################ ..
.. #                                 GITHUB                                   # ..
.. ############################################################################ ..

Getting Git
-----------

The `latest version of AIMBAT <https://github.com/pysmo>`_ will be on Github, so it would be good to get `Git <https://github.com/>`_ on your computer. This is not strictly necessary, as you could also download it as a zipfile from the `AIMBAT website <http://www.earth.northwestern.edu/~xlou/aimbat.html>`_.

Some users may already have Git installed, but if not, you can download the package installer `here <http://git-scm.com/download/mac>`_. This would allow only command line usage of Git, so if you want to use a GUI, we recommend `Git for Mac <https://mac.github.com/>`_. 

.. ############################################################################ ..
.. #                                 GITHUB                                   # ..
.. ############################################################################ ..









.. ############################################################################ ..
.. #                              OPERATING SYSTEM                            # ..
.. ############################################################################ ..

Getting your operating system
-----------------------------

We assume that most users of AIMBAT will be using macs. If our assumptions are wrong, please :ref:`contact the authors <authors-contacts>`, and if there is sufficient interest we will construct documentation for installations on other operating systems as well. 

On a mac, to find the version of your operating system, first click on the apple icon on the top bar of your desktop, go to ``System Preferences``, and click on ``Startup Disk``. The operating system version should then be displayed. 

.. image:: installing-images/system_preferences.png

.. ############################################################################ ..
.. #                              OPERATING SYSTEM                            # ..
.. ############################################################################ ..






.. ############################################################################ ..
.. #                            PYTHON DEPENDENCIES                           # ..
.. ############################################################################ ..

Python Packages needed
----------------------

The following are required for AIMBAT
* `Numpy <http://www.numpy.org/>`_
* `Scipy <http://www.scipy.org/>`_
* `Matplotlib <http://matplotlib.org/>`_


Using `iPython <http://ipython.org/>`_ is optional but recommended, as iPython is an interactive console designed to make 

.. ############################################################################ ..
.. #                            PYTHON DEPENDENCIES                           # ..
.. ############################################################################ ..






.. ############################################################################ ..
.. #                             ENTHOUGHT CANOPY                             # ..
.. ############################################################################ ..

Installing Python
-----------------

`Enthought Canopy <https://www.enthought.com/store/>`_ is easy to install. Go to `the website <https://www.enthought.com/store/>`_ and download the free version of Express Enthought Canopy, which will give you the dependencies Numpy, Scipt, and Matplotlib.

.. ############################################################################ ..
.. #                             ENTHOUGHT CANOPY                             # ..
.. ############################################################################ ..







.. ############################################################################ ..
.. #                       INSTALLING PYTHON - MACPORTS                       # ..
.. ############################################################################ ..

If you cannot use Enthought Canopy
----------------------------------

This section describes a possible way to install Python without using Enthough Canopy. It is `not` recommended and may cause problems on some systems, but the authors describe it just in case. 

Usually, Macs already have python installed by default. To check if you have python on your mac, open up terminal, and type ``python``. If python is installed, a console should pop up. If python is not installed, you should see an error message show up. You should download the correct verion for your operating system `here <https://www.python.org/>`_. 

.. -------------------------------------------------------------------------------- ..

Getting Macports
~~~~~~~~~~~~~~~~

Its best to use `Macports <http://guide.macports.org/>`_ to install the necessary python libraries for AIMBAT. If you just upgraded your operating system, you need to `upgrade Macports and re-install the libraries <https://trac. macports.org/wiki/Migration>`_ as well. 

.. -------------------------------------------------------------------------------- ..

Installing the necessary components
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Inside the terminal, once python is install, type these commands in using sudo mode. Note you will need to enter your admin password.::

	sudo port install python27
  sudo port install py27-numpy
  sudo port install py27-scipy
  sudo port install py27-matplotlib
 	sudo port install py27-ipython
  sudo port install python_select

Installing the last two packages is optional. ``ipython`` is an enhanced interactive python shell. ``python_select`` is used to select default Python version by the following command::

	port select --set python python27

You need this version, not other versions on your computer, since this is the one that has the libraries AIMBAT needs.


.. ############################################################################ ..
.. #                       INSTALLING PYTHON - MACPORTS                       # ..
.. ############################################################################ ..






.. ############################################################################ ..
.. #                         REGARDING PACKAGE MANAGERS                       # ..
.. ############################################################################ ..

Regarding Package Managers
--------------------------

The package manager brew caused many problems when tried. If you figured it out properly, please :ref:`contact the authors <authors-contacts>` with instructions~ In general, the authors do not recommend trying to install the packages separately when there are Python versions that will come with all the packages pre-installed already.

`Scipy <http://www.scipy.org/install.html>`_ is especially tricky as it relies on Fortran and C as well. The authors of scipy recommend using Enthought Canopy or Anacoda to install it.

.. ############################################################################ ..
.. #                         REGARDING PACKAGE MANAGERS                       # ..
.. ############################################################################ ..





.. ############################################################################ ..
.. #                           INSTALLING BASEMAP                             # ..
.. ############################################################################ ..

Installing Basemap
------------------

Disclaimer: Lifted from content written by `this guy <http://blog.bluedackers.com/2012/11/13/installing-basemap-on-mac-os-x-mountain-lion/>`_ with some tweaks. 

Enthough Python should get you most of the dependencies needed. You do need to get `Geos <http://trac.osgeo.org/geos/>`_ though. The best way to get it is `install Homebrew <http://matthewcarriere.com/2013/08/05/how-to-install-and-use-homebrew/>`_, and then install ``gdal``, a package that has ``Geos`` as a dependency. To get ``gdal``, do::

  brew install gdal

Now install Basemap. Download it `here <http://sourceforge.net/projects/matplotlib/files/matplotlib-toolkits/>`_. Unzip the package and cd into the unzipped package. Export the directory where ``Geos`` was installed::

  export GEOS_DIR=/usr/local/Cellar/geos/3.4.2/

And install Basemap::

  sudo python setup.py build
  sudo python setup.py install

To check it worked, at the terminal, do::
  
  python

and then::

  from mpl_toolkits.basemap import Basemap

.. ############################################################################ ..
.. #                           INSTALLING BASEMAP                             # ..
.. ############################################################################ ..




.. ############################################################################ ..
.. #                              POSSIBLE ISSUES                             # ..
.. ############################################################################ ..

Possible Issues
---------------

Here some common problems and possible resolutions. If your problem is not listed here, or you have a suggestion, please :ref:`contact the authors <authors-contacts>`.

.. -------------------------------------------------------------------------------- ..

Macport 
~~~~~~~

You may run into problems with AIMBAT if your `Macport <http://www.macports.org/>`_ version is not compatible with your operating system version. For example, if you used Macports for OS X 10.8 to install AIMBAT, then upgraded your operating system or OS X 10.9, you may find that AIMBAT no longer works properly. You will need to upgrade Macports to fix this error.

Do not uninstall MacPorts unless you know what you are doing, uninstalling MacPorts may get rid of other programs you installed using MacPorts. However, if you are sure you want to do so, see `here <https://guide.macports.org/chunked/installing.macports.uninstalling.html>`_ for instructions.

.. -------------------------------------------------------------------------------- ..

Installing Python with Pip
~~~~~~~~~~~~~~~~~~~~~~~~~~

Be careful with the operating system. For OS X 10.9 and above, Python 2.7 is not fully compatible and there may be problems installing python with Pip. Best to use Enthought Canopy or Python 3 with OS X 10.9.

.. -------------------------------------------------------------------------------- ..

Setting the Python Path to the scripts
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

You are asked to add the path to the AIMBAT scripts in your file. To do that, you add them to the ``.bashrc`` file. There are other files you could add it to that work as well, such as the ``.profile`` or ``.bash_profile`` files. You can see the files by opening the terminal and doing ``ls -a`` to see all the hidden files, and open then by doing ``vi .bashrc`` in vim, for instance.
To ensure you can open a script, you need to add::

  	export PATH=$PATH:<path-to-folder-with-scripts>
  	export PYTHONPATH=$PYTHONPATH:<path-to-folder-with-scripts>

to the ``.bashrc`` file. We recommend adding the paths to the ``.bashrc`` file.

.. -------------------------------------------------------------------------------- ..

Terminal Commands stop working
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

If ever the terminal commands such as ls stop working in the terminal, it could be that something went wrong with a path in the ``.bashrc`` or ``.profile`` files. If that happens you may not be able to open them in vim as that command would have stopped working as well. Instead, in the terminal, you do::

  PATH=/bin:${PATH}
  PATH=/usr/bin:${PATH}

And that should allow the commands to start working again. Figure out what you did wrong and remove that command.

.. -------------------------------------------------------------------------------- ..

Installing Enthought Canopy
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Occasionally, Enthought Canopy may not open the default setup environment after you downloaded and tried to install it. If this happens, open the Canopy package, go to "Preferences", and select Canopy as your default environment.

.. image:: installing-images/enthought_as_default.png

.. -------------------------------------------------------------------------------- ..

Uninstalling Enthought Canopy
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The official Enthought gives suggestions on uninstalling `here <https://guide.macports.org/chunked/installing.macports.uninstalling.html>`_.

.. image:: installing-images/canopy_preferences.png

STEPS:

#. From the Canopy preferences menu, unset Canopy as your default Python.
#. For each Canopy user, delete the following directory which contains that user’s "System" and "User" virtual environment subdirections.
#. Delete Canopy from the Applications folder.
#. Clean up the hidden files. Delete anything referencing Canopy or Enthought in the hidden files, as evidence by referencing ``ls -a`` in your home directory. Check the ``.bashrc`` and ``.profile`` directories first. If Enthought is not completely gone, this happens if you call Python.
#. (Optional). Keep doing ``which python`` and cleaning the python files that show up, until ``which python`` gives you nothing when you type it in the terminal.

.. image:: installing-images/applications_canopy.png

.. -------------------------------------------------------------------------------- ..

Path to python files not found
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

After adding the path to your directory with scripts in ``.bashrc``, you still need to source the ``.bashrc`` files in ``.profile``, or the system may not find the directory. See here for more `details <http://publib.boulder.ibm.com/infocenter/pseries/v5r3/index.jsp?topic=/com.ibm.aix.baseadmn/doc/baseadmndita/prof_file.htm>`_ to see how the profile file is sourced. Note that this one will override the file in `/etc/profile`.

.. image:: installing-images/residue.png

.. image:: installing-images/profile_file.png

`This explanation <http://linux.die.net/man/1/bash>`_ explains how the bashrc file is sourced.

.. image:: installing-images/bashrc_file.png


This is what the bashrc and profile files should look like on your home directory:

.. image:: installing-images/bashrc_home.png

.. image:: installing-images/profile_home.png


.. ############################################################################ ..
.. #                              POSSIBLE ISSUES                             # ..
.. ############################################################################ ..









































































