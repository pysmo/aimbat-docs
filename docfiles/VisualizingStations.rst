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

You can get some example data to test this out by downloading the Github repository `data-example <https://github.com/pysmo/data-example>`_. Now, cd into the folder `example_pkl_files`, which has several mcp files containing the results of picking travel wave arrival times on a set of seismograms. 

Run `getsta.py` on the PKL file to get the file `loc.sta` containing the station locations. For example, in `data-example/example_pkl_files` type::
	
	getsta.py 20120101.05275598.bhz.pkl

This will output a file, `loc.py`.

Next, run `mccc2delay.py` to convert the MCCC delays into actual delays. For example, in `data-example/example_pkl_files` type::

	mccc2delay.py 20120101.05275598.bhz.pkl

You will get a `.px` file. 

To plot the stations colored by delay times, run `doplotsta.sh <file-name>.px`. For example, in `data-example/example_pkl_files` type::

	doplotsta.sh 20120101.05275598.px




