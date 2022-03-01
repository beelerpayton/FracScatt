Functions for Forward Mie Calculations of Homogeneous Spheres
=============================================================

Functions for single particles
---------------------------------

.. py:function:: MieQ(m, wavelength, diameter[, nMedium=1.0, asDict=False, asCrossSection=False])

   Computes Mie efficencies *Q* and asymmetry parameter *g* of a single, homogeneous particle. Uses :py:func:`Mie_ab` to calculate :math:`a_n` and :math:`b_n`, and then calculates *Q* via:
   
		:math:`${\displaystyle Q_{ext}=\frac{2}{x^2}\sum_{n=1}^{n_{max}}(2n+1)\:\text{Re}\left\{a_n+b_n\right\}}$`
		
		:math:`${\displaystyle Q_{sca}=\frac{2}{x^2}\sum_{n=1}^{n_{max}}(2n+1)(|a_n|^2+|b_n|^2)}$`
		
		:math:`${\displaystyle Q_{abs}=Q_{ext}-Q_{sca}}$`
		
		:math:`${\displaystyle Q_{back}=\frac{1}{x^2} \left| \sum_{n=1}^{n_{max}}(2n+1)(-1)^n(a_n-b_n) \right| ^2}$`
		
		:math:`${\displaystyle Q_{ratio}=\frac{Q_{back}}{Q_{sca}}}$`
		
		:math:`${\displaystyle g=\frac{4}{Q_{sca}x^2}\left[\sum\limits_{n=1}^{n_{max}}\frac{n(n+2)}{n+1}\text{Re}\left\{a_n a_{n+1}^*+b_n b_{n+1}^*\right\}+\sum\limits_{n=1}^{n_{max}}\frac{2n+1}{n(n+1)}\text{Re}\left\{a_n b_n^*\right\}\right]}$`
		
		:math:`${\displaystyle Q_{pr}=Q_{ext}-gQ_{sca}}$`
		
   where asterisks denote the complex conjugates.
   
   **Parameters**
   
   
   m : complex
	The complex refractive index, with the convention *m = n+ik*.
   wavelength : float
	The wavelength of incident light, in nanometers.
   diameter : float
	The diameter of the particle, in nanometers.
   nMedium : float, optional
	The refractive index of the surrounding medium. This must be positive, nonzero, and real. Any imaginary part will be discarded.
   asDict : bool, optional
	If specified and set to True, returns the results as a dict.
   asCrossSection : bool, optional
	If specified and set to True, returns the results as optical cross-sections with units of nm\ :sup:`2`.
	
   **Returns**
   
   
   qext, qsca, qabs, g, qpr, qback, qratio : float
	The Mie efficencies described above.
   cext, csca, cabs, g, cpr, cback, cratio : float
	If asCrossSection==True, :py:func:`MieQ` returns optical cross-sections with units of nm\ :sup:`2`.
   q : dict
	If asDict==True, :py:func:`MieQ` returns a dict of the above efficiencies with appropriate keys.
   c : dict
	If asDict==True and asCrossSection==True, returns a dict of the above cross-sections with appropriate keys.
