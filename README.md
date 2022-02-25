
# Competition | Airbnb Prices


## Introduction
The idea behind this repository is to find the best machine learning model and params for a given dataset of Airbnb adds.
Airbnb is the web with the wider amount of adds for rent by days for mainly touristic projects. 

The projects was based on a dataset called `train.csv`, from which a prediction on prices for a dataset called `test.csv` needed a ML model to be based on or to model. 

## Processing and cleaning 

The dataset was form with 37 columns and more than 4000 files, which were giving many information on the flat and the host. 

For cleaning I decided to leave out a lot of columns, with the pandas function `pd_to_numeric`, and i ended up with the following:
'id', 'host_listings_count', 'latitude', 'longitude', 'accommodates', 'price', 'maximum_nights', 'minimum_nights_avg_ntm',       'maximum_nights_avg_ntm', 'availability_90', 'number_of_reviews'.

A function for getting the numerical value of the baths and host superhost was also done, adding these two columns:
'bathrooms', 'superhost'

From the columns, it was missing two important and very relatable information, the areas of the city and the room type. therefore it was  done a `pd.dummy` on those two columns.  However, in the execution of the machine learning models, those values were not as good as without them for the final score. 


## Models
Once I cleaned the dataset, I decided to use from `sklearn` library the model Xgboost model, to definde a linear tree in which the model will analyse the data and predict the price according to the same data columns. 

Then i decided to use the H2O model, which will stack different models and give me the most accurate prediction. 

For seeing the whole code, you can find the jupyter notebook here [https://github.com/evaarquero/airbnb_kaggle/blob/master/Airbnb_models.ipynb]


