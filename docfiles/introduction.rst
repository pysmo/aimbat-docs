Introduction
============

AIMBAT (Automated and Interactive Measurement of Body wave Arrival Times) is an open-source software package for efficiently measuring teleseismic body wave arrival times for large seismic arrays.

It is based on a widely used method called MCCC (Multi-Channel Cross-Correlation). The package is automated in the sense of initially aligning seismograms for MCCC which is achieved by an ICCS (Iterative Cross Correlation and Stack) algorithm.

Meanwhile, a GUI (graphical user interface) is built to perform seismogram quality control interactively. Therefore, user processing time is reduced while valuable input from a user's expertise is retained. As a byproduct, SAC plotting and phase picking functionalities are replicated and enhanced.

Modules and scripts included in the AIMBAT package were developed using `Python programming language <http://www.python.org/>`_ and its open-source modules on the Mac OS X platform since 2009. The original MCCC code was transcribed into Python.

The GUI of AIMBAT was inspired and initiated at the `2009 EarthScope USArray Data Processing and Analysis Short Course <http://www.iris.edu/hq/es\_course/>`_.

AIMBAT runs on Mac OS X, Linux/Unix and Windows thanks to the platform-independent feature of Python. 
It's been tested on Mac OS 10.6.8 and 10.7 and Fedora 16.

The AIMBAT software package is distributed under the `GNU General Public License Version 3 (GPLv3) <http://www.gnu.org/licenses/gpl.html>`_ as published by the Free Software Foundation.