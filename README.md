


Data generation
The data generation folder contains 6 Jupyter notebooks. Gen Data is the primary notebook and should be read first. All 6 notebooks are identical except for some minor differences. Notebooks with the suffix "Re" are the same as their counterparts except that the user bid rule was changed to 90% of true value. Gen data exp and Gen data exp 1 1 vary the number of bidders, competitor bid distributions, and auction rule parameters.

Data
The data folder contains 24 csv files which are subsequently used to create 2 dataframes of 1008 observations each.

Feat engineering
This notebook transforms the data files into one dataframe which is then scaled and train/test split.

Modeling and CV
Two separate classifications are attempted, with K-Fold CV Testing of KNN, Logistic Regression, Decision Tree, Random Forests, Support Vector Machines, and XG Boost. Next, the test data is used for the top performing models, and confusion matrices are produced. 

Data Viz
TBD
