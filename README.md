# Modeling the Kaggle West Nile Prediction Competition


Weather data is used as the main feature set, and time series aggregations were used for modeling (mean, max, etc. over various time windows).  Record leakage (the fact that multiple rows are included in the test data when mosquitoes were found) was leverage to create features used in modeling (this isn't a useful approach for true prediction, however it's tested for fun here anyways).  Also, no LB tuning was done to account for the year to year differences in WN prevalence or outbreaks.

![I'm a pic](https://github.com/jfunk2968/WestNile-Kaggle/blob/master/skeeter_pic.jpg)


The code is still as it was used during development and meant as an example of work (i.e. it hasn't been cleaned up to simply produce the final solution).  

### This repo contains the following IPython notebooks:
1.  WN-Explore.ipynb - an initial exploration of the provided data files 
2.  WN-Model.ipynb - the main notebook used to explore the data and develop models
3.  WN-Weather_Features.ipynb - creates a dataframe of time dependent weather features used in modeling
4.  WN-Record_Features.ipynb - creates features that exploit the record leakage nature of the competition data
5.  WN-Record_Geo_Features.ipnb - creates features based on record leakage of nearby locations
