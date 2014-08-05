aimbat-docs
===========

* Documentation for AIMBAT, hosted by [Sphinx](http://sphinx-doc.org/).
* Read the docs [here](http://aimbat.readthedocs.org/en/latest/).

Dependencies
------------
* Sphinx
* Some form of browser
* [LaTeX](http://www.latex-project.org/) 

Building
--------
cd into the repository `aimbat-docs`, and run:
````
  sphinx-build -b html . builddir
  make html
  make latexpdf
````

Remember to run these commands *before* you push to Github during each build!

It takes a while for the online docs to build and configure after you have pushed to Github.
