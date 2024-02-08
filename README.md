# Machine Learning - Regression Modeling for Predicting Real Estate Housing Prices in Ames, Iowa

Hello, thank you for taking a look at my machine learning project on housing data prediction. This dataset is from a study that Dean De Cock used to repalce the classic Boston Housing Data in regression analysis. The data used in this project is a bit different from his original dataset since we had some extra records to add to the dataset to assist with training & testing. (2580 rows x 82 columns)

For an easy visualization of my project, I put together a google slides presentation. View it here: https://docs.google.com/presentation/d/1F5N20jnKmLapszeNSPAwbf0-6eQdejuNab831QpbaTQ/edit#slide=id.g2b644170a95_0_17420

There are suggestions in his original paper around removal of certain data which I incorporate into my modeling.
You can find the original paper here: https://jse.amstat.org/v19n3/decock.pdf

I developed models by separating 3 data transformations in different notebooks, ordinal, dummified, and dummified without a column drop. The way I cleaned and transformed the data can be found in the folders labeled 'data_cleaning'

In addition to 3 data transformations, I also tested 3 different methods of filtering the data for outliers. That will be shown in 'model_building'. One method was removing 3 * IQR for SalePrice, a second was removing SalesCondition != 'Normal' (as per De Cock's suggestion), and a third was to not touch the outliers at all.

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

In my presentation I go into tradeoffs of choosing a best model vs. a more explainable one. However if you want to view the stacked model, it can be found in 'model_building'. I use scikit-learn's StackedRegressor to form a level 0 model with my highest performing catboost_tuned, xgboost_tuned, and ridge model, then use linearRegression at level 1 for the best score in the study. 

Take a look at the ordinalCatBootViz notebook for some explainable model visualizations! There are also some visualizations in the data cleaning notebooks, particularly the original.

Please feel free to reach out with any questions on my project or code, I am more than happy to chat. 

-B
