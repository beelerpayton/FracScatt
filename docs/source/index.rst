.. FracScatt documentation master file, created by
   sphinx-quickstart on Mon Feb 28 21:38:26 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
   

Online user's guide for the Python Fractal Scattering package (PyFracScatt)
======================================================================

Documentation is always under development, but mostly complete. A manuscript communicating the development of the inverse Mie algorithms was published by the `Journal of Quantative Spectroscopy and Radiative Transfer <http://www.sciencedirect.com/science/journal/00224073>`_. The JQSRT article is `available here <https://doi.org/10.1016/j.jqsrt.2017.10.012>`_.

**NOTE TO USERS:** When using PyMieScatt, pay close attention to the units of the your inputs and outputs. Wavelength and particle diameters are always in nanometers, efficiencies are unitless, cross-sections are in nm\ :sup:`2`, coefficients are in Mm\ :sup:`-1`, and size distribution concentration is always in cm\ :sup:`-3`. If you use other units, your outputs may not make sense.

**NOTE TO THOSE WITH MIEPLOT EXPERIENCE:** The functions in PyMieScatt take particle *diameter*. MiePlot's default is to take the particle *radius* in micrometers. Make sure all your particle dimensions, whether for a single particle or for a distribution, are for the diamaters, in nanometers.


Install PyMieScatt
------------------

NOTE: You must install `Shapely <https://shapely.readthedocs.io/>`_ first, preferably from GitHub. Users have reported difficulty installing it with pip. Conda works, too.

The current version is 1.8.0. You can install PyMieScatt from `The Python Package Index (PyPI) <https://pypi.python.org/pypi/PyMieScatt>`_ with ::

   $ pip install PyMieScatt


or from `GitHub <https://github.com/bsumlin/PyMieScatt>`_. Clone the repository and then run ::

   $ python setup.py install
