# Heston_SV_Calibration
This is a replica of Yiran Cui, Sebastian del Baño Rollin, Guido Germano's paper--[Full and fast calibration of the Heston stochastic volatility model](https://eprints.lse.ac.uk/83754/1/Germano_Full%20and%20fast%20calibration_2017.pdf)
## Key technical skills:
1. They compared different versions of the characterisation function of the Heston process (since the complex logarithm is multivalued), and they found a good version compared to the past ones.
2. They used an analytical gradient instead of a numerical gradient.
3. Vectorised integration in the Heston gradient.
4. Calibration using the Levenberg-Marquardt method.


## Snapshot of result:
* Initial guess: [ 1.2  0.2  0.3 -0.6  0.2]
* Optimisation success: True
* Estimated parameters: [ 3.    0.1   0.25 -0.8   0.08]
* True parameters: [ 3.    0.1   0.25 -0.8   0.08]
* Time elapsed: 1.5494 seconds
