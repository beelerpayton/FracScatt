Morphology Retrieval for Internally Mixed Black Carbon Aggregates
=============================================================

Functions for single particles
---------------------------------

.. py:function:: SingleParticle(coating, absorption, wavelength, diameter[, abs_error=0.0, mode='Mtot_Mbc', r_monomer=20.0])

   Computes core phase shift parameter :math:`{\left(\rho_{BC}\right)}` of fractal black carbon aggregates. Uses particle diameter :math:`{\left(d_p\right)}`, mass absorption cross-section :math:`{\left(MAC_{BC}\right)}`, and mixing state :math:`{\left(M_{tot}/M_{BC}\right)}`, and calculates :math:`{\rho_{BC}}` by first determining whether the measured :math:`{MAC_{BC}}` is significantly less than that predicted by:
   
	:math:`{MAC_{BC}=MAC_0\left (\frac{\lambda}{\lambda_0} \right)^{-AAE}\left[1+\frac{AC^{-B}\Gamma(B+1,C)}{C}-\frac{A\left(\frac{M_{tot}}{M_{BC}}\right)^{B}\left(\frac{M_{tot}}{M_{BC}}\right)^{-B}\Gamma\left(B+1,C\frac{M_{tot}}{M_{BC}}\right)}{C}\right]}`
	
	- :math:`{A=-1.189\pm0.029}`
	- :math:`{B=-0.674\pm0.006}`
	- :math:`{C=0.043\pm0.0007}`
	- :math:`{MAC_0=6.819\pm0.131}`
	- :math:`{AAE=1.231\pm0.005}`
	
   If :math:`{MAC_{BC}}` is close to the value predicted by the above equation, then :math:`{\rho_{BC}}` can be constrained to 0 < :math:`{\rho_{BC}}` < 1, but cannot be exactly calculated. If the measured :math:`{MAC_{BC}}` is less than what is predicted by the above equation, :math:`{\rho_{BC}}` is then calculated via: 
   
	:math:`{MAC_{BC}=MAC_0\left (\frac{\lambda}{\lambda_0} \right)^{-AAE}\left[\frac{D}{E+1}\left(\rho_{BC}^{1-E}-1\right)\right]}`
   
   
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
	- 'Mtot_Mbc' : ratio of total particle mass to black carbon mass
	- 'Rbc' : ratio of coating mass to black carbon mass
	- 'OC:EC' : ratio of organic carbon mass to black carbon mass
	- 'percent_BC' : percentage of total particle mass which is attributed to black carbon.
	
	
   **Returns**
   
   
   mass, rho : float
	The Mie efficencies described above.
   fig : figure
	Figure showing morphology retrival.
	
