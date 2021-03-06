# Source code for R replication of XYZ Model 

This repository contains the code for the xyz project, which is split into two components:

1. Estimation
2. Simulation

## 1. Estimation

The estimation component estimates a set of behavioral equations and calculate empirical distirbutions to be used as inputs into the simulation component of the model.

- The `1.cleandata.R` file takes the `fmla_2012_employee_restrict_puf.csv` data as input, creates a number of variables required for the estimation procedures and saves the `fmla_clean_2012.csv` file.

- The `2.estimate_behavioral.R` file taks the `fmla_clean_2012.csv` data as input and estimates a number of logit regressions. The resulting parameter estimates are saved as csv files in the `estimates` folder.

- The `3.estimate_distributions.R` file taks the `fmla_clean_2012.csv` data as input and calculates a number of leave length distributions, which is then saves as csv files in the `estimates` folder.

## 2. Simulation

The simulation component uses the parameters derived from the estimation component to simulate the leave taking behavior of individuals within the ACS.
