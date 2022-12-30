.. pyBCabsorption documentation master file, created by
   sphinx-quickstart on Mon Feb 28 21:38:26 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
   

Online user's guide for the Python Black Carbon Absorption package (pyBCabs)
======================================================================

Documentation is always under development, but mostly complete. A manuscript communicating the development of the morphology retrival was published by `Atmospheric Chemistry and Physics <https://www.atmospheric-chemistry-and-physics.net>`_, and is `available here <https://doi.org/10.5194/acp-22-14825-2022>`_.

**NOTE TO USERS:** When using pyBCabsorption, pay close attention to the units of the your inputs. Wavelength and particle diameters are always in nanometers, mass absorption cross-sections are in m\ :sup:`2`/g. If you use other units, your outputs may not make sense.


Install pyBCabs
------------------

The current version is 0.0.1. You can install pyBCabs from `The Python Package Index (PyPI) <https://pypi.python.org/pypi/pyBCabs>`_ with ::

   $ pip install pyBCabs==0.0.1

or from `GitHub <https://github.com/beelerpayton/pyBCabs>`_. Clone the repository and then run ::

   $ python setup.py install

  
Revision History
----------------

- 0.0.1 (30 December, 2022)

  - Initial release.
  
Author Contact Information
--------------------------
pyBCabs was written by `Payton Beeler <https://scholar.google.com/citations?user=8Td-XI4AAAAJ&hl=en&oi=ao/>`_.

Email: `beelerpayton@wustl.edu <mailto:beelerpayton@wustl.edu?subject=pyBCabs>`_


.. toctree::
   :maxdepth: 2
   :caption: Table of Contents
   
   Documentation Home <index>
   Functions <functions>
   Example Scripts <examples>
