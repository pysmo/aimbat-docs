=============
Plot Stations
=============

.. ############################################################################ ..
.. #                             PLOT STATIONS                                # ..
.. ############################################################################ ..

Plot Stations
-------------

Click on the `Plot Stations` button and you will get a graph of all the stations for the set you are using. Stations used are the red circles, and deleted stations not used in the cross-correlation are the black triangles.

.. ############################################################################ ..
.. #                             PLOT STATIONS                                # ..
.. ############################################################################ ..



.. ############################################################################ ..
.. #                          COLOR BY DELAY TIMES                            # ..
.. ############################################################################ ..

Color By Delay Times
--------------------

* On the terminal, cd into the same folder where you sourced the SAC files to run ``ttpick.py``, after running ``MCCC`` on a pickle file name, for instance, ``20120123.16045298.pkl``, you will get a mcp file named ``20120123.16045298.mcp``. 

* Run ``mccc2pkl.py 20120123.16045298.mcp`` and you will get a file with travel times called ``20120123.16045298.dtp``.

* Run ``doplotsta.sh`` and you will get a two ``gif`` files of the stations colored by delay times.

.. image::plot-stations/delay_times.png




.. ############################################################################ ..
.. #                           COLOR BY DELAY TIMES                           # ..
.. ############################################################################ ..