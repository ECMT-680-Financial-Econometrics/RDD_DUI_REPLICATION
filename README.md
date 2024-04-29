# RDD_DUI_REPLICATION
This repository is a  replication of the paper "Punishment and Detterrence: Evidence From Drunk Driving" by Benjamin Hansen, published in the National Bureau of Economic Research. The study uses the different thresholds for a DUI (0.08 BAC) and aggravated DUI (0.15 BAC) as cutoffs for a Regression Discontinuity Design analysis in order to examine recidivism (the tendency of a criminal to reoffend). 

"Regression discontinuity derived
estimates suggest that having a BAC above the DUI threshold reduces recidivism by up to 2 percentage
points (17 percent). Likewise having a BAC over the aggravated DUI threshold reduces recidivism
by an additional percentage point (9 percent)" (Hansen).

In this repository there is: 

modified_hansen_data.csv - This is a .csv file used for the replication. The original data file was called 'hansen_dwi.csv', however we modified this file to add two new columns: 'dui' and 'agg_dui'. 'dui' is a binary variable that takes the value of 1 if 'bac1' is between 0.08 and 0.15, and 0 otherwise. 'agg_dui' is a binary variable that takes the value of 1 if 'bac1' is over 0.15 and 0 otherwise. The variable 'bac2' was ignored in this replication due to the methodology of Scott Cohn, who did a replication of this paper and decided to ignore 'bac2'.

hansen-2015-punishment-and-deterrance-evidence-from-drunk-driving.pdf - The actual paper itself

RDD_Graphs_MachineLearning.ipynb - This is a .ipynb file containing Python code used for the replication of graphs from the study, as well as our machine learning enhancements of the study.

RDD_Results_Replication.ipynb - This is a .ipynb file containing Python code used for the replication of the actual numerical results of the study. In this file, a Weighted Least Squares (WLS) model is used to estimate the effect of 'dui' and 'agg_dui' on recidivism at 3 different bandwiths: 0.05, 0.025, and our optimal bandwith calculated with machine learning.

RDD_Project_ECMT_680(4).pdf - Our poster presentation giving a basic summary of results.
