=============================
Visualizing Stations on a map
=============================

Coloring stations by delay times
--------------------------------

* On the terminal, cd into the same folder where you sourced the SAC files to run ``ttpick.py``, after running ``MCCC`` on a pickle file name, for instance, ``earthquake-event.pkl``, you will get a mcp file named ``earthquake-event.mcp``. 

* Run ``mccc2delay.py earthquake-event.mcp`` and you will get a file with travel times called ``earthquake-event.dtp``.

* Run ``doplotsta.sh`` and you will get a two ``gif`` files of the stations colored by delay times.

.. image::plot-stations/delay_times.png

Computing delay times
---------------------

The equation used to compute delays is explained here [BulandChapMan1983]_. 

