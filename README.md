<br />
<p align="center">
  <h3 align="center">Communities and Violent Crime</h3>

  <p align="center">
    Tested six varieties of supervised learning regression models and optimized the most promising to predict the rate of violent crime in U.S. communities per 100K residents. Used 122 community attributes as features, drawn from U.S. Census data, the annual U.S. LEMAS (law enforcement) survey, and the FBI's UCR.  In selecting a preferred model, interpretability and accuracy were both considered, as the goal of the project is to understand correlates of violent crime in cities.
    <br />
    <br />
    <a href="https://colab.research.google.com/drive/1Jr4WnqwSiqNEGMnRRoMf6Z5JTx6uOMty?usp=sharing">View Notebook</a>
  </p>
</p>


<!-- ABOUT THE PROJECT -->
## About The Project

I chose to tackle this project because of ongoing conversations around violent crime and policing in cities around the U.S. during the summer of 2020.


### Built With

* []() Scikit-Learn
* []() Scipy.stats
* []() Numpy
* []() <a href="https://archive.ics.uci.edu/ml/datasets/Communities+and+Crime+Unnormalized">Data</a> compiled for the UCI Machine Learning Repository


## Feature Engineering

The dataset consisted of data from 2,215 cities and metropolitan areas in the U.S.  Unfortunately, policing data, which was of strong interest in the project, had been withheld for 84% of communities and so was not included in the models.  (This led to a rabbit hole of police data research.)  I addressed nulls and missing values in the data, examined the features for collinearity and automated feature selection retaining 26 community attributes, and transformed the data somewhat to reign in outliers.


## Model Building

I created a success metrics function that displays R^2, MAE, MSE, RMSE, and MAPE for each model run.  I then preliminarily tested regression models including decision tree, random forest, K-nearest neighbors, support vector machines, gradient boosting with regression trees, and linear models to get an idea of which ones perform best with this data.  Random forest, gradient boosting with regression trees, and linear regression showed the most promise.  

I tuned each of those models using GridSearchCV and tried ridge, lasso, and ElasticNet linear regressions, finding that gradient boosting with regression trees yielded the lowest errors and highest predictive value.  However, because interpretability was one of my goals in undertaking the project, my model of choice was simple OLS linear regression because it provided coefficients and p-values for each of the 26 features and allowed me to see what features are most important in predicting violent crime rates.  Importantly, the R^2 values for the best models reached only ~60%, implying that violent crime cannot be fully predicted in terms of the included community attributes.  Most interestingly to me, neither poverty nor its close correlate, education, are the highest predictors of violent crime.


## Future Work

Contribute to organizations that advocate for transparency of police department data.
