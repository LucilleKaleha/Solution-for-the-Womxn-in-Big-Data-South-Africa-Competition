## [Lucille Kaleha ](https://www.linkedin.com/in/lucillekaleha/): **Second position solution for the Womxn in Big Data South Africa competition**


---
*Thanks to Zindi, Women in Big Data, HERE Technologies and Microsoft for this challenge and opportunity to improve livelihoods using Data Science*

### Challenges faced:
 - Feature engineering did not yield good results
 - There was no correlation between local cross validation and the leaderbaord, so it was challenging to know how good a model is and whether it was overfitting
 - Using all the data for training yielded worse results
 - It was very challenging to get new data from the recommended HERE and XYZ apis.
 
### Approach used:
 - Focused more on bulding models rather than feature engineering
 - As location was an important feature, i reverse geocoded the coordinates to get locations for each latitude and longitude using the reversegeocoding python library
 - As there was no single model that yielded good results, i opted to train several models so that they can cancel each others errors and generalize well
 - Because using all the data yielded unsatisfactory resultes, i opted to train each model with 70% of the data
 - To ensure that all the data has been used for training, i used different random states to split the data
 - Finally to generalise the ensembled models; I averaged, blended and retrained the models using the test data as training data and predictions as the target
 
### Some small caveats:
 - I realised that using different versions of catboost regressor yielded different results, so i maximised on this and used two versions of catboost.
    - At some point in the notebook you will have to restart the kernel.
 - Setting the random states(seed) did help for reproducability, but some models dont have the random state parameter, so there is some bias/randomness that cannot be accounted for. So predictions will differ by a small margin whenever you run the notebook.
 

