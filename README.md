# Random Forest in Equity classification

In this project, we apply Random forest model to analyze composition of Portfolios.
We only release 


## Raw Data preprocessing and Features selection
In order to have balanced and meaningful feature of each stocks, we calculate some meaningful features from raw data. With raw data at hand, we recommend calculating meaningful features so that the training result is reasonable.

### Feature list
We Calculate Beta for each Sector. 
E(R<sub>i</sub>) = &beta;<sub>1</sub>E(R<sub>Tech</sub>) + &beta;<sub>2</sub>E(R<sub>Utility</sub>) + ... + &beta;<sub>1</sub>E(R<sub>Financial</sub>) + &epsilon;


Market Cap, Sector Betas, Volatility, EV/Asset Ratio, P/E Ratio, ...etc.


## Model training
Use GridSearchCV from sklearn to search the optimal hyperparameter (we use 5-fold cross validation and Roc_Auc as evalutating score).<br>
Use RandomForestClassifier as classifier.<br>
In order to get balance training set, we use upsampling tecnique. <br>
Save trained models by pickle.

## Result
We get over 95% accuracy on sector prediction, and average 84% accuracy on other metrics prediction.


## Authors
Wuzhe Xu

