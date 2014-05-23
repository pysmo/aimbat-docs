=======================
Parameter Configuration 
=======================

Backend
-------

`Matplotlib <http://matplotlib.org/contents.html>`_ works with six GUI (Graphical User Interface) toolkits:
#. WX
#. Tk
#. Qt(4)
#. FTK
#. Fltk
#. macosx

The GUI of AIMBAT uses the following to support interactive plotting:
#. `GUI neutral widgets <http://matplotlib.org/api/widgets_api.html>`_
#. `GUI neutral event handling API (Application Programming Interface) <http://matplotlib.org/users/event_handling.html>`_

Examples given in this documentation are using the default toolkit ``Tk`` and backend ``TkAgg``. 

Visit these pages for an `explanation of the backend <http://matplotlib.org/faq/usage_faq.html#what-is-a-backend>`_ and `how to customize it <http://matplotlib.org/users/customizing.html#customizing-matplotlib>`.

**Put the following line in you ``matplotlibrc`` file:**::

	backend : TkAgg #Agg rendering to a Tk canvas

Other parameters for the package can be set up by a configuration file ``ttdefaults.conf``, which is interpreted by the module ConfigParser. This configuration file is searched in the following order:

#. file ``ttdefaults.conf`` in the current working directory
#. file ``.aimbat/ttdefaults.conf`` in your ``HOME`` directory
#. a file specified by environment variable ``TTCONFIG``
#. file ``ttdefaults.conf`` in the directory where AIMBAT is installed

Python scripts in the ``<pkg-install-dir>/pysmo-aimbat-0.1.2/scripts`` can be executed from the command line. The command line arguments are parsed by the optparse module to improve the scripts' exibility. If conflicts existed, the command line options override the default parameters given in the configuration file ``ttdefaults.conf``. Run the scripts with the ``-h`` option for the usage messages.
