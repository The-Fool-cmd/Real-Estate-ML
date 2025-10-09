### Author: Sandu Petru-Calin
# Part 2 of this ML project

#### I've done EDA while preprocessing the dataset to get to my final feature matrix:
1. Cut down the dataset to 8 columns at first before proceeding into EDA.
2. Cut out the rows which didn't have a property type as they can't be used to help the model.
3. Remove the Address and Date fields as they can't help the model.
4. Noticing how greatly assessed value and sale amount can vary i applied a log transform which greatly helped.
5. Merged the Property Type and Residential Type since the latter was redundant.
6. Removed outliers with IQR.
7. One-encoding for top 15 towns and top 8 property types, removing all other rows.
8. Prepare X and y for modelling.
9. Ran 3 models to compare performance:
Linear Regression: +/-44.7%
Random Forest Regressor: +/-34.9%
History Gradient Boosting Regressor: +/-34.3%

Observations:
The model seemed to plateau at the 0.295 Test RMSE value. I believe this may be due to the high variance of the dataset and the instability of real estate prices even in a given city.
The rest of my thoughts can be found in part_2.ipynb
