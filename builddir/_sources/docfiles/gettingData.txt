============
Getting Data
============

The material in this section is `not` needed to install AIMBAT and get it working if you already have the SAC files you want to use AIMBAT on. If you may need to 

There are several ways to obtain seismic data from `IRIS <http://www.iris.edu/dms/nodes/dmc/data/types/waveform-data/>`_ to input to AIMBAT. The authors used two ways to do it, and a further list of libraries for obtaining seismic data is provided in the sidebars `here <http://www.iris.edu/dms/nodes/dmc/data/types/waveform-data/>`_. 

.. ############################################################################ ..
.. #                           OBSPY CLIENT FDSN                              # ..
.. ############################################################################ ..

Obspy.fdsn for downloading data
-------------------------------

Installing Obspy
~~~~~~~~~~~~~~~~

We recommend using Macports to install Obspy as detailed in the `Installation` section `here <https://github.com/obspy/obspy/wiki>`_. If you have installed Enthough Canopy::

    sudo port install py27-obspy

should do it. If not, installing with `Homebrew <https://github.com/obspy/obspy/wiki/Installation-on-OS-X-using-Homebrew>`_ also seems to work. 

Did the installation work?
~~~~~~~~~~~~~~~~~~~~~~~~~~

If installation has worked, `close the terminal` you used to install Obspy on, and then open it again. Now, open the Python terminal in a new terminal, and type::

    import obspy

If there are no errors, your installation has worked. 

Using Obspy
~~~~~~~~~~~

Use the `Obspy FDSN <http://docs.obspy.org/packages/obspy.fdsn.html#>`_ Web service client for Obspy in Python. Once you have done so, check out the `SAC-Input Output <http://docs.obspy.org/packages/obspy.sac.html>`_ libraries for loading the data to Python and saving it as SAC or Pickle files. 


.. ############################################################################ ..
.. #                           OBSPY CLIENT FDSN                              # ..
.. ############################################################################ ..








.. ############################################################################ ..
.. #                        STANDING ORDER FOR DATA                           # ..
.. ############################################################################ ..

Standing Order for Data
-----------------------

From the `SOD <http://www.seis.sc.edu/index.html>`_ website:

    Standing Order for Data, is a framework to define rules to select seismic events, stations, and data. It then allows you to apply processing to the events, stations, and data and currently contains a large set of rules that allow you to select with great precision in these items. The processes mainly consist of simple data transformation and retrieval, but SOD defines hooks to allow you to cleanly insert your own processing steps, either written in Java or an external program.

Installing SOD
~~~~~~~~~~~~~~

First, download `SOD <http://www.seis.sc.edu/index.html>`_.

Once you have gotten the folder for SOD, put it somewhere where you won't touch it too much. What I did was put the SOD folder in my home directory, though other places are acceptable as well, as long as its not too easy to delete it by accident.

.. image:: sod-images/sod_location.png

Once you have it there, get the path to the sod folder's bin and put it in your path folder. 

.. image:: sod-images/path_to_sod_bin.png

Inside my home directory's bash profile (you get the by typing `cd`), you put the path to `sod-3.2.3/bin` by adding in either the `bash` or `bash_profile` or `profile` files.




.. ############################################################################ ..
.. #                        STANDING ORDER FOR DATA                           # ..
.. ############################################################################ ..












