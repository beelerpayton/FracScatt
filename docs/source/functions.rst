Morphology Retrieval for Internally Mixed Black Carbon Aggregates
=============================================================

Functions for single particles
---------------------------------

.. py:function:: SingleParticle(coating, absorption, wavelength, diameter[, abs_error=0.0, mode='Mtot_Mbc', r_monomer=20.0])

   Computes core phase shift parameter :math:`{\rho_{BC}}` of fractal black carbon aggregates. Uses particle diameter :math:`{d_p}`, mass absorption cross-section :math:`{MAC_{BC}}`, and mixing state :math:`{M_{tot}/M_{BC}}`, and calculates :math:`{\rho_{BC}}` via:
   
	:math:`{MAC_{BC}=MAC_0\left (\frac{\lambda}{\lambda_0} \right)^{-AAE}\left[1+\frac{AC^{-B}\Gamma(B+1,C)}{C}-\frac{A\left(\frac{M_{tot}}{M_{BC}}\right)^{B}\left(\frac{M_{tot}}{M_{BC}}\right)^{-B}\Gamma\left(B+1,C\frac{M_{tot}}{M_{BC}}\right)}{C}\right]}`
   
   
   **Parameters**
   
   
   coating : float
	Ratio of total particle mass to black carbon mass.
   absorption : float
	The mass absorption cross-section with units of m\ :sup:`2`/g.
   wavelength : float
	The wavelength of incident light, in nanometers.
   diameter : float
   	The volume-equivalent diameter, in nanometers.
   abs_error : float, optional
	The errors associated with mass absorption cross-section measurement.
   mode : string, optional
	Available options:
	1. 'Mtot_Mbc' : ratio of total particle mass to black carbon mass\n
	2. 'Rbc' : ratio of coating mass to black carbon mass
	3. 'OC:EC' : ratio of organic carbon mass to black carbon mass
	4. 'percent_BC' : percentage of total particle mass which is attributed to black carbon.
	
	
   **Returns**
   
   
   mass, rho : float
	The Mie efficencies described above.
   fig : figure
	Figure showing morphology retrival.
