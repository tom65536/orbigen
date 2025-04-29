Host Star
=========

Simplification
--------------

To keep the following derivation and the code simple
a single host star is assumed. Any higher multiplicity
systems are disregarded.

Assumptions
-----------

One may expect the star to be stable over
a time long enough for complex life to develop.
The only reference we have is life on earth, where the
formation of the planet and formation of complex life
took



The host star should possess a habitable zone according
to the constraints defined in :cite:`Schwieterman_2019`
for supporting complex life forms. Therefore  minimum
surface temperature of 3700 Kelvin (:math:`0.64T_0`) is assumed.

Using the relations for main sequence stars given
in the appendixb we may specify a mass bound instead
of a temperature,

.. math::

   0.64=\frac{T}{T_0}=\left(\frac{M}{M_0}\right)^{0.42}


.. literate-code:: define minimum surface temperature
   :lang: python

   SOLAR_TEMP = 5780.0
   MIN_STAR_TEMP = 3700.0
   MIN_STAR_TEMP_REL = MIN_STAR_TEMP / SOLAR_TEMP
   MIN_STAR_MASS_REL = MIN_STAR_TEMP_REL ** (1.0/0.42)


.. literate-code:: star.py
   :file:
   :lang: python

   """Generation of the host star."""

   {{define minimum surface temperature}}

