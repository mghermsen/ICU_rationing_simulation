# ICU_rationing_simulation

This script accepts a clean, long form patient dataset and generates a set of inputs for a discrete event microsimulation model of ICU rationing.




# SOFA Coding Details

To standardize SOFA coding between sites, please follow the 


## SOFA CARDS
Only number of pressors matters, not dose.

* 2 or more pressors -> 4
* 1 pressor -> 3
* Dobutamine alone -> 2
* Map < 70 -> 1
* MAP >70, no pressors -> 0


## SOFA respiratory
Ignore respiratory support, i.e. level of mechanical ventilation

If PaO2/FiO2 Is not available, use SaO2/FiO2:
* SF<=150 -> 4
* SF 150-235 -> 3
* SF 235-315 ->  2
* SF 315-400 -> 1

