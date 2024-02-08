Hello, thank you for taking a look at my machine learning project on housing data prediction. This dataset is from a study that Dean De Cock used to repalce the classic Boston Housing Data in regression analysis. The data used in this project is a bit different from his original dataset since we had some extra records to add to the dataset to assist with training & testing. (2580 rows x 82 columns)

There are suggestions in his original paper around removal of certain data which I incorporate into my modeling.
You can find the original paper here: https://jse.amstat.org/v19n3/decock.pdf

I developed models by separating 3 data transformations in different notebooks, ordinal, dummified, and dummified without a column drop. The way I cleaned and transformed the data can be found in the folders labeled 'data_cleaning'

In addition to 3 data transformations, I also tested 3 different methods of filtering the data for outliers. That will be shown in 'model_building'.

The actual model building and scoring process can be found in the notebooks under 'model_building', I labeled each by the regression method or algorithm I used. For the tree based models you will find two separate for loops that generate the models, the first will be the name of the algorithm, such as 'xgboost', and the next will be the tuned version, such as 'xgboost_tuned'. 

For methods and algorithms, the list I utilize is: 

MLR
Lasso
Ridge
Elastic Net
Gradient Boosting 
Random Forest

(not from scikit-learn)
XGBoost 
CatBoost

I evaluated two ways to tune the models I used, which can be viewed in the OptunaTesting notebook. I use scikit-learn's GridSearchCV and Optuna.


-B
