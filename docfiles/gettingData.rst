============
Getting Data
============

Note: Not necessary if you already have your own set ways of obtaining data. This section is added for completeness. 

There are several ways to obtain seismic data from `IRIS <http://www.iris.edu/dms/nodes/dmc/data/types/waveform-data/>`_ to input to AIMBAT. The authors used two ways to do it, and a further list of libraries for obtaining seismic data is provided in the sidebars `here <http://www.iris.edu/dms/nodes/dmc/data/types/waveform-data/>`_. 

.. ############################################################################ ..
.. #                           OBSPY CLIENT FDSN                              # ..
.. ############################################################################ ..

Obspy.fdsn for downloading data
-------------------------------

Installing Obspy
~~~~~~~~~~~~~~~~

We recommend using Macports to install Obspy as detailed in the `Installation` section `here <https://github.com/obspy/obspy/wiki>`_. If you have installed Enthought Canopy::

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

Note: NOT needed for AIMBAT, but important to know about as it is a commonly used package for downloading seismic data with the user's specifications. Although Obspy also offers was to download seismic data from IRIS, SOD allows for better fine-tuning of data obtained. 

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

Example SOD recipe
~~~~~~~~~~~~~~~~~~

Inside the repository `data-example <https://github.com/pysmo/data-example>`_, there is a folder `sod_requests`. The file within it called `sod_request.xml`, which is available `here <https://github.com/pysmo/data-example/blob/master/sod_requests/sod_request.xml>`_, is an example of a sod request recipe that will download data from IRIS. To run it, cd into the folder containing `sod_request.xml`, and do::

	sod sod_request.xml

Downloading the data (output as SAC files) may take a while. This receipt filters the data, and outputs the folders `processedSeismograms` and `seismograms`, which container the filtered and unfiltered data.  



.. ############################################################################ ..
.. #                        STANDING ORDER FOR DATA                           # ..
.. ############################################################################ ..












