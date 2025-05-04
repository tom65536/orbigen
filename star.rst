Host Star
=========

Simplification
--------------

To keep the following derivation and the code simple
a single host star is assumed. Any higher multiplicity
systems are disregarded.

Assumptions
-----------

In order to have a realistic chance to encounter
complex life on the plnet its host starOne should
be stable over a time long enough for complex life
to develop.
The only true reference we have is life on earth, where the
formation of the planet and formation of complex life
on land took of the order of 4.3 billion years.

During this period the host star should remain on the
main sequence avoiding catastrophic events endangouring
life on the planet.

Inverting the
:ref:`mass-life-time relation <mass-lifetime-relation>`
from the appendix
we can derive an upper mass limit.

.. math::


  \frac{M_0}{M}=\left(\frac{10^{10}y}{4.3\times10^9y}\right)^{0.4}

Hence the mass of the hast star should not exceed 1.4
solar masses.

.. literate-code:: define maximum stellar mass
   :lang: python

   MAX_STAR_MASS_REL = 1.4

Furthermore, the host star should possess
a habitable zone according
to the constraints defined in :cite:`Schwieterman_2019`
for supporting complex life forms. Therefore  minimum
surface temperature of 3700 Kelvin (:math:`0.64T_0`) is assumed.

Using the relations for main sequence stars given
in the appendix we may specify a mass bound instead
of a temperature,

.. math::

   0.64=\frac{T}{T_0}=\left(\frac{M}{M_0}\right)^{0.42}


.. literate-code:: define minimum stellar mass
   :lang: python

   SOLAR_TEMP = 5780.0
   MIN_STAR_TEMP = 3700.0
   MIN_STAR_TEMP_REL = MIN_STAR_TEMP / SOLAR_TEMP
   MIN_STAR_MASS_REL = MIN_STAR_TEMP_REL ** (1.0/0.42)


.. literate-code:: star.py
   :file:
   :lang: python

   """Generation of the host star."""

   {{define minimum stellar mass}}
   {{define maximum stellar mass}}
