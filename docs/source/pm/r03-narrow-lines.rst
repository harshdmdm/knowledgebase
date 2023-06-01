R03: Calculating Narrow Lines
=============================

This assumes that you have observations in a Narrow Band filter and a Broad Band Filter that underlies (in wavelength) the Narrow Band Filter. The calculations assume that only one emission or absoprtion line is significant within the range of the broad band filter from the line source, and that the underlying continuum is well represented by other continuum sources in the image. 

Terms that are used:
--------------------

:math:`f_B` the flux in the Broad Band Filter (e.g. B, V, R, I) \\
:math:`f_N` the flux in the Narrow Band Filter (e.g. Ha, OIII, SII)


:math:`f_C` the continuum flux \\
:math:`f_L` the line flux


:math:`k` the observed filter scaling factor

Note that the fluxes that emerge will be in the same units as the fluxes in the broad band filter.

Steps
-----

First select a continuum source (or better repeat for several continuum sources) e.g. stars in your image. Your goal here is to find the conversion factor :math:`k` that allows you to scale between the broad and narrow filters.

*For the continuum source:*

.. math::

   f_B &= f_C \\
   f_N &= kf_C \\
   f_N / f_B &= k
   
When you have found your value for k (or average value for k, which is of course more reliable), you can look at your source of interest, which we want to break down into line and continuum fluxes.

*For the line + continuum source:*

.. math::

   f_B &= f_C + f_L \\
   f_N &= (kf_C) + f_L \\
   f_B - f_N &= f_C (1-k) \\
   f_C &= (f_B - f_N) / (1-k) \\
   f_L &= f_B - f_C = f_B - (f_B - f_N) / (1-k) \\
   (1-k)f_L &= f_B - kf_B - f_B + f_N \\
   f_L &= (f_N - kf_B) / (1-k)
   
so you have now measured the Line flux from the source, separated from the continuum flux.
   
