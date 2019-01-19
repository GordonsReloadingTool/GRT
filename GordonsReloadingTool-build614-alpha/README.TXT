GORDONS RELOADING CHANNEL
https://youtube.com/GordonsReloading
gordonsreloading@gmail.com

================================================================================
 G O R D O N S  R E L O A D I N G  T O O L
 I N T E R I O R  B A L L I S T I C S
================================================================================
  Copyright (c) Gordons Reloading Channel, all rights reserved
  Commercial use without written permission is strictly prohibited.

--------------------------------------------------------------------------------
!!! A T T E N T I O N !!!
------------------------------------------------------------------------
THE PROGRAM IS AN INTERIOR BALLISTIC SIMULATION RELOAD TOOL.
CURRENTLY A DEVELOPMENT VERSION! THE SOFTWARE IS UNFINISHED!

USE AT YOUR OWN RISK! THESE PROGRAMS DO NOT REPLACE ANY LOAD TABLES, SPECIALIST
BOOKS AND MANUFACTURER RECOMMENDATIONS! THE DISPLAYED/CALCULATED RESULTS MUST
BE COMPARED WITH CURRENT LOADING TABLES AND LOADING RECOMMENDATIONS OF THE
MANUFACTURERS OF THE COMPONENTS USED! ANY LIABILITY AND WARRANTY RESULTING
DIRECTLY OR INDIRECTLY FROM THE USE OF THESE PROGRAMS AND THEIR CALCULATIONS
IS EXCLUDED, EVEN IN THE EVENT OF NEGLIGENCE.

THE CALCULATION RESULTS CAN BE INCORRECT! THE CALCULATED PRESSURES AND
VELOCITIES CAN DEVIATE STRONGLY FROM REAL MEASURED VALUES. NC-POWDER DEVIATES
SIGNIFICANTLY FROM THE MATHEMATICALLY SPECIFIED BURN-UP BEHAVIOUR AT LOW
PRESSURES, SO THE RESULTS BECOME LESS ACCURATE AT LOW PRESSURES WITH A SMALL
AMOUNT OF PROPELLANT CHARGE.

NO WARRANTIES ARE MADE AS TO THE SUITABILITY OF THE INFORMATION PROVIDED BY THE
PROGRAM OR DOCUMENTS CONTAINED THEREIN. THE PROGRAM AND RELATED DOCUMENTS AND
DATA ARE "AS IS" AND ARE PROVIDED "AS IS" WITHOUT WARRANTIES OF ANY KIND, EITHER
EXPRESS OR IMPLIED. WITH RESPECT TO APPLICABLE LAW, ALL WARRANTIES, EXPRESS OR
IMPLIED, INCLUDING, BUT NOT LIMITED TO, IMPLIED WARRANTIES OF MERCHANTABILITY
AND FITNESS FOR A PARTICULAR PURPOSE, OWNERSHIP AND NON-VIOLATION OF RIGHTS.

--------------------------------------------------------------------------------

 The mention of product names of other manufacturers in the following text
 is for information purposes only and is therefore not marked separately.
 The corresponding names are partly protected trademarks and are also recognized
 as such.

--------------------------------------------------------------------------------
EXPLANATION (and how it came about)
--------------------------------------------------------------------------------
This software is the result of my research into the interior ballistic
calculation on the basis of a mathematical simulation model.

Internally, a simulation calculation is made which calculates the combustion
of the powder, the resulting gases, pressures and energy on the basis of a
formalism based on scientific research, the development of which in turn goes
back over 100 years.

The chemical energy released by the conversion of the propellant charge is
essentially split up during combustion:

 - translational projectile energy
 - rotatory projectile energy
 - Flow energy of the powder gases
 - Internal energy of powder gases
 - Heat losses at tube, bullet and sleeve
 - Friction and heat transfer
 - Work against the pull-out resistance
 - Work on pressing the bullet into the trains
 - Energy of the returning weapon parts
 - Energy for propulsion of (semi-)automatic weapons

The proportion of the weapon's recoil and, where appropriate, the propulsion
energy of automatic weapons in the total energy is less than 1% overall and is
therefore neglected.

The flow energy of the powder gases can be adjusted by adding a of the cargo
(carrying factor, Sebertian factor) to which the accelerating bullet mass in
the invoice. So you calculate, as is usual in other areas of physics, with an
effective mass. Also other losses of energy can be calculated here by effective
mass such as energy losses due to heat dissipation.

ORIGIN/REFERENCES

Primarily, the algorithms in the base are based on information that is
can be found in Rheinmetall's "Waffentechnische Taschenbuch". There, an example
is given to describe in detail what such a calculation could look like. Apart
from the fact that this paperback is also very interesting, the software
"QuickLOAD" also uses the same identifiers for the corresponding base values,
e.g. "Ba" for the burnup coefficient and much more. Since in more modern
literature other identifiers are usually used, which resemble each other
strikingly, it is quite difficult to find the right one. plausible that the
formalism in QuickLOAD also exactly those algorithms which have been published
in Rheinmetall's weapons technology pocketbook can be shown in simplified form.

If you are interested, look for the title

"Rheinmetall Waffentechnisches Taschenbuch" (german)

In the Waffentechnisches Taschenbuch, from page 70 onward, the interior
ballistic Calculation explained in detail including an example. The differential
equations are to be understood as a BASIS for the calculations. They treat the
case for a propellant powder that burns evenly, because the equations for it
are much simpler.

The different propellant powders have different burning characteristics,
i.e. depending on the type, the powder burns in the course of the pressure
development with DIFFERENT fast speed! Such powders are then progressive,
degressive or a combination thereof. The terms 'progressive' and 'offensive'
are not mutually exclusive here, because even an offensive powder can
are very progressive.

With the different burning behaviour it can be influenced whether e.g.
a projectile is accelerated more strongly in a longer barrel and simultaneously
but the pressure can stay low.

This characteristic is specified by a so-called FORM FUNCTION and these
Form function then describes mathematically approximated the behavior of the
Powder during combustion. FOR A CORRECT IMPLEMENTATION YOU HAVE TO SOLVE THE
DIFFERENTIAL EQUATION FROM THE POCKETBOOK NEW WITH BUILT-IN FORM FUNCTION.
This is what i try with the test program and it seems that this is also
accurate and successful.

You can now see the result of my inquisitiveness in this calculation programs.

Gordon
06.01.2019
