============
Unit Testing
============

This section is mainly for those who which to make tweaks to AIMBAT themselves. We have added some unit tests to AIMBAT to ensure its robustness. 

.. ############################################################################ ..
.. #                          GETTING THE PACKAGES                            # ..
.. ############################################################################ ..

Getting the Dependencies
------------------------

We are using `PyUserInput <https://github.com/SavinaRoja/PyUserInput>`_ to simulate matplotlib GUI events, which in turn requires Quartz and AppKit for Mac users. 

To install Quartz and AppKit, we recommending doing the following as suggested `here <http://stackoverflow.com/questions/21359285/no-module-named-appkit>`_::
	
	sudo pip install pyobjc-core
	sudo pip install pyobjc

To check that you have successfully installed them, inside the Python console do::

	import AppKit
	import Quartz

and ensure there are no errors.

To import PyUserInput, we recommend running::

	sudo pip install PyUserInput



.. ############################################################################ ..
.. #                          GETTING THE PACKAGES                            # ..
.. ############################################################################ ..