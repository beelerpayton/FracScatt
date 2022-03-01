.. FracScatt documentation master file, created by
   sphinx-quickstart on Mon Feb 28 21:38:26 2022.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.
   

Online user's guide for the Python Fractal Scattering package (PyFracScatt)
======================================================================

DELETE THIS LATER. Documentation is always under development, but mostly complete. A manuscript communicating the development of the morphology retrival was published by the `Journal Name <http://www.sciencedirect.com/science/journal/00224073>`_, and is `available here <https://doi.org/10.1016/j.jqsrt.2017.10.012>`_.

**NOTE TO USERS:** When using PyFracScatt, pay close attention to the units of the your inputs. Wavelength and particle diameters are always in nanometers, mass absorption cross-sections are in m\ :sup:`2`/g. If you use other units, your outputs may not make sense.


Install PyFracScatt
------------------

The current version is 0.0.1. You can install PyFracScatt from `The Python Package Index (PyPI) <https://pypi.python.org/pypi/PyFracScatt>`_ with ::

   $ pip install PyFracScatt

or from `GitHub <https://github.com/beelerpayton/PyFracScatt>`_. Clone the repository and then run ::

   $ python setup.py install

Revision Notes
----------------

- 0.0.1 (28 February, 2022)

  - Debugging and troubleshooting.
  
Revision History
----------------

- 0.0.1 (28 February, 2022)

  - Debugging and troubleshooting.
  
Author Contact Information
--------------------------
PyFracScatt was written by `Payton Beeler <https://scholar.google.com/citations?user=8Td-XI4AAAAJ&hl=en&oi=ao/>`_.

Email: `beelerpayton@wustl.edu <mailto:beelerpayton@wustl.edu?subject=PyFracScatt>`_


.. toctree::
   :maxdepth: 2
   :caption: Table of Contents
   
   Documentation Home <index>
   Morphology Retrieval <functions>
   Example Scripts <examples>
