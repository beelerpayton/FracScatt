Morphology Retrieval for Internally Mixed Black Carbon Aggregates
=============================================================

Theory 
---------------------------------

   This package computes core phase shift parameter :math:`{\left(\rho_{BC}\right)}` and infers the morphology of fractal black carbon aggregates. First, using the particle diameter :math:`{\left(d_p\right)}`, mass absorption cross-section :math:`{\left(MAC_{BC}\right)}`, and mixing state :math:`{\left(M_{tot}/M_{BC}\right)}`, :math:`{\rho_{BC}}` is constrained by determining whether the measured mass absorption cross-section :math:`{\left(MAC_{BC,measured}\right)}` is significantly less than that given by:
   
	:math:`{MAC_{BC,predicted}=MAC_0\left (\frac{\lambda}{\lambda_0} \right)^{-AAE}\left[1+\frac{AC^{-B}\Gamma(B+1,C)}{C}-\frac{A\left(\frac{M_{tot}}{M_{BC}}\right)^{B}\left(\frac{M_{tot}}{M_{BC}}\right)^{-B}\Gamma\left(B+1,C\frac{M_{tot}}{M_{BC}}\right)}{C}\right]}`
	
	- :math:`{A=-1.189\pm0.029}`
	- :math:`{B=-0.674\pm0.006}`
	- :math:`{C=0.043\pm0.0007}`
	- :math:`{MAC_0=6.819\pm0.131}`
	- :math:`{AAE=1.231\pm0.005}`
	
   If :math:`{MAC_{BC,measured}}` is within 10% of :math:`{MAC_{BC,predicted}}`, then :math:`{\rho_{BC}}` can be constrained to 0 < :math:`{\rho_{BC}}` < 1, but cannot be exactly calculated. If :math:`{MAC_{BC,measured}}` is more than 10% less than :math:`{MAC_{BC,predicted}}`, then :math:`{\rho_{BC}}` is calculated by solving: 
   
	:math:`{MAC_{BC,measured}=MAC_0\left (\frac{\lambda}{\lambda_0} \right)^{-AAE}\left[\frac{D}{E+1}\left(\rho_{BC}^{1-E}-1\right)+\frac{D}{1-2E}\left(\rho_{BC}^{1-2E}-1\right)\right]+MAC_{BC}|_{\rho_{BC<1}}}`

   Where :math:`{D}` and :math:`{E}` are sigmoid functions, given by:
   
   	:math:`{X=x_1+\frac{x_2-x_1}{1+\text{exp}\left[x_3\left(\rho_{BC}-x_4\right)\right]}}`
	
   Here :math:`{X}` represents :math:`{D}` or :math:`{E}` and :math:`{x_{[1,2,3,4]}}` represents :math:`{d_{[1,2,3,4]}}` or :math:`{e_{[1,2,3,4]}}`. 
   
	- :math:`{d_1=5.679\pm0.027}`
	- :math:`{d_2=1.066\pm0.058}`
	- :math:`{d_3=0.264\pm0.010}`
	- :math:`{d_4=11.421\pm0.137}`
	- :math:`{e_1=2.440\pm0.017}`
	- :math:`{e_2=0.593\pm0.024}`
	- :math:`{e_3=0.418\pm0.020}`
	- :math:`{e_4=10.106\pm0.131}`
   
   
   The single particle mass is determined from the provided :math:`{\left(d_p\right)}`. Details on the derivation of the above equations are `available here <https://doi.org/10.1016/j.jqsrt.2017.10.012>`_.


Functions for single particles
---------------------------------

.. py:function:: SingleParticle(coating, absorption, wavelength, diameter[, abs_error=0.0, mode='Mtot_Mbc', r_monomer=20.0])

   The single particle mass is determined using the provided :math:`{\left(d_p\right)}`, assuming the density of black carbon is 1.8 g/cm\ :sup:`3`.
   
   **Parameters**
   
   coating : float
	Ratio of total particle mass to black carbon mass.
   absorption : float
	The mass absorption cross-section with units of m\ :sup:`2`/g.
   wavelength : float
	The wavelength of incident light, in nanometers.
   diameter : float
   	The volume-equivalent diameter of the black carbon core, in nanometers.
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
	
