===============
SAC Data Access
===============


.. ############################################################################ ..
.. #                         PYTHON OBJECT FOR SAC FILE                       # ..
.. ############################################################################ ..

Python Object for SAC File
--------------------------

The ``pysmo.sac`` package is developed to read and write individual SAC files.
The Python class ``sacfile`` of module ``sacio`` opens a SAC file and returns an object including data and all SAC header variables as its attributes. Modifications of object attributes are saved to file. It is written purely in Python so that it also runs with `Jython <http://www.jython.org>`_.
  	
`egsac.py`
~~~~~~~~~~

The ``<pkg-install-dir>/aimbat/scripts/egsac.py`` script gives a simple example to read, resample and plot a seismogram using pysmo, Scipy and Matplotlib. You can type the codes in a Python/iPython shell, or run as a script in the data example directory `<pkg-install-dir>/data-example/example_pkl_files/Event_2011.09.15.19.31.04.080`.

.. image:: SACdataAccess/prog-egsac.png

Resampling Seismograms
~~~~~~~~~~~~~~~~~~~~~~

In this example, a SAC file named `TA.109C.\_\_.BHZ.sac` is read in as a sacfile object. The time array is calculated from SAC headers.  The data array is resampled from interval 0.025 to 2.0 seconds using Scipy's signalprocessing module.

Add the following codes to write the resampled seismogram to file `TA.109C.\_\_.BHZ.sac`::

	sacobj.delta = deltanew
	sacobj.npts = nptsnew
	sacobj.data = y2

.. image:: SACdataAccess/egsac-109c.pdf

.. ############################################################################ ..
.. #                         PYTHON OBJECT FOR SAC FILE                       # ..
.. ############################################################################ ..










