# A Solution for the Kaggle West Nile prediciton competition


Weather data is used as the main feature set, and time series aggregations were used for modeling (mean, max, etc. over various time windows).  Record leakage (the fact that multiple rows are included in the test data when moquitos were found) was leverage to create features used in modeling.  This isn't a useful approach for true prediction, however I used it anyways. Also, no LB tuning was done to account for the year to year differences in WN prevalance or outbreaks.


The code is still as it was used during development (i.e. it hasn't been cleaned up to simply produce the solution).  

###This repo contains the following IPython notebooks:
1.  WN-Model.ipynb - the main notebook used to explore the data and develop models
2.  WN-Weather_Features.ipynb - creates a dataframe of time dependent weather features used in modeling
3.  WN-Record_Features.ipynb - creates features that exploit the record leakage nature of the competition data
4.  WN-Record_Geo_Features.ipnb - creates features based on record leakage of nearby locations
