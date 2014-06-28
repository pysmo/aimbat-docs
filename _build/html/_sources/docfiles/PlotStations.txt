=============
Plot Stations
=============

.. ############################################################################ ..
.. #                             PLOT STATIONS                                # ..
.. ############################################################################ ..

Plot Stations
-------------

Click on the ``Plot Stations`` button and you will get a graph of all the stations for the set you are using. Stations used are the red circles, and deleted stations not used in the cross-correlation are the black triangles.

.. image::plot-stations/basemap_stations.png

.. ############################################################################ ..
.. #                             PLOT STATIONS                                # ..
.. ############################################################################ ..



.. ############################################################################ ..
.. #                          COLOR BY DELAY TIMES                            # ..
.. ############################################################################ ..

Color By Delay Times
--------------------

Instructions
~~~~~~~~~~~~

* On the terminal, cd into the same folder where you sourced the SAC files to run ``ttpick.py``, after running ``MCCC`` on a pickle file name, for instance, ``earthquake-event.pkl``, you will get a mcp file named ``earthquake-event.mcp``. 

* Run ``mccc2delay.py earthquake-event.mcp`` and you will get a file with travel times called ``earthquake-event.dtp``.

* Run ``doplotsta.sh`` and you will get a two ``gif`` files of the stations colored by delay times.

.. image::plot-stations/delay_times.png

Learn more about how to compute delay times
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

The equation used to compute delays is explained here [BulandChapMan1983]_. 


.. ############################################################################ ..
.. #                           COLOR BY DELAY TIMES                           # ..
.. ############################################################################ ..