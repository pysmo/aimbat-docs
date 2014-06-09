==============
Filtering Data
==============

There are several options for filtering data. `SAC <http://www.iris.edu/files/sac-manual/>`_ offers several ways to filter data, which are not discussed here. You could also do so when downloading data using SOD. Alternatively, you could filter data in AIMBAT. 


.. ############################################################################ ..
.. #                                   GUI                                    # ..
.. ############################################################################ ..

Filtering GUI
-------------

To filter data, once you have imported the files to run into the GUI, hit the ``filter`` button to bring up the filtering GUI. The figure on top shows the results of the signal plotted against time before and after filtering with a `butterworth filter <http://en.wikipedia.org/wiki/Butterworth_filter>`_. 

.. image::filtering-data/filter_interface.png

You can adjust the corner frequencies used on the figure on the lower corner. The defaults used here are:

+----------------+----------+
| Variable       | Default  |
+================+==========+
| Order          | 2        |
+----------------+----------+
| Filter Type    | Bandpass |
+----------------+----------+
| Low Frequency  | 0.05 Hz  |
+----------------+----------+
| High Frequency | 0.25 Hz  |
+----------------+----------+

You can change the order and filter type by selecting the option you want. By clicking on the lower figure, you can select the low frequency and the high frequency you want. Click ``apply`` to filter the seismograms when you are satisfied with the filter paramters chosen.

.. ############################################################################ ..
.. #                                   GUI                                    # ..
.. ############################################################################ ..





.. ############################################################################ ..
.. #                               SAVING OPTIONS                             # ..
.. ############################################################################ ..

Saving Options
--------------

There are several options for saving the SAC header files of the seismograms you have chosen. 

+----------------------------------+----------------------------------------------------+
| Button Title                     | What it does                                       |
+==================================+====================================================+
| Save Headers Only                | Saves the SAC headers only                         |
+----------------------------------+----------------------------------------------------+
| Save Headers & Filter Parameters | Saves the SAC headers and filter parameters used.  |
|	                           | Those filter parameters will automatically the     |
|	                           | next time the SAC headers are loaded in AIMBAT     |
+----------------------------------+----------------------------------------------------+
| Save Headers & Override Data     | Save SAV headers and write in the filtered data    |
+----------------------------------+----------------------------------------------------+

.. image::filtering-data/saving_types.png

.. ############################################################################ ..
.. #                               SAVING OPTIONS                             # ..
.. ############################################################################ ..
