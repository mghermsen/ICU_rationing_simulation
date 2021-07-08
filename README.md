# ICU rationing simulation

This script accepts a clean, long form patient dataset and generates a set of inputs for a discrete event microsimulation model of ICU rationing.




## SOFA Coding Details

To standardize SOFA coding between sites, please follow the best practices below.


### SOFA CARDS
Only number of pressors matters, not dose.

* 2 or more pressors -> 4
* 1 pressor -> 3
* Dobutamine alone -> 2
* Map < 70 -> 1
* MAP >70, no pressors -> 0


### SOFA respiratory
Ignore respiratory support, i.e. level of mechanical ventilation

* P/F <=100 -> 4
* P/F 100-200 -> 3
* P/F 200-300 ->  2
* P/F 300-400 -> 1
* P/F >400 -> 0

If PaO2/FiO2 Is not available, use SaO2/FiO2:
* SF<=150 -> 4
* SF 150-235 -> 3
* SF 235-315 ->  2
* SF 315-400 -> 1
* SF >400 -> 0

