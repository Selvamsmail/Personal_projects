
# Factors Influencing Home Prices Across The United States

This project focuses on finding the features that influence the house price over a decade. since this the task involves time as a factor, taking a normal house price data will not be a reliable messure. 
so we have taken the index price data. During the data preprocessing,
the values had a lot of multi-coliniearity we still retained the values because our aim was not on the prediction of future but to understand 
the economic contribution and the factors that might involve a role in the price change of houses. we have built 2 models such as linear regression and XGBOOST.
Regression is to find the linear pattern and also to find the best feature contribution.
XGBOOST is an ensemble technique, we have used to regrously train the model and obtain the best contributing feature from that.
The evaluation technique we have used is Cross validation as our data is not very large though we have taken a month wise data. 
the most important feature was the Consumer price index and then the Stock price and followed by the population.
with the compleation of this project we can get a hint of what are the important features to consider on the prediction of a decade's house price in the future.




## DATA
### Discription of the DATA.

The dataset used to find the feature importance involves 
index price of houses, stock price, population, Unemployment_Rate,
Real_GDP, Mortgage_Rate, Real_Disposable_Income.
the data is collected from Kaggle. It includes 423
observations of the price changes and messures of population and economic factors collected from Fred.
date of the data ranges from 1998 till 2022 may.

the data was obtained from following link.

https://www.kaggle.com/code/faryarmemon/factors-affecting-usa-home-prices/data?select=Housing_Macroeconomic_Factors_US+%282%29.csv

### DATA PREPROCESSING

there was not a lot to pre-process the data it had no null values.
the data was already processed.
just that there was a feature extraction required and the date column was actully an object.
we have extracted the year from all the dates as all the other info is not a lot helpfull.

## Visualizations.

The year was the timeline factor. so trying to analyse the trend and also the change taking place we have plotted the following plot.

![trend](https://user-images.githubusercontent.com/98254459/209277214-953076ce-075d-4688-83f9-a56810030057.png)

Through this plot we can build many insight on the change in various features over time.

house price index had a drop in 2010 and kept increasing till 2022. 

consumer price and the population was the factors that kept increasing.

we also see that we have a drop in mortgage rates constantly.

GDP has been constant and started fluctuating a lot in covid and the war times...(after 2020)
not in the scope of the project though.

though unemployement rate is not stable we would prot a corr matrics to have a look.

### Multicollinearity

The Multicollinearityis important factor when we are going to build a linear reg model.

since a strong corelation with other features may lead the model to not diferentiate the target from features.

![corr](https://user-images.githubusercontent.com/98254459/209278096-599961d8-86d2-48ef-97a9-ed166adf5487.png)

we definately see a lot of Multicollinearity in the data.
since this project is to analyse the contributing factors to price change.
we are not droping this features or the project. in gendral the features should not have Multicollinearity more than 0.8
here we have till 0.9. we will still use the linear regression for the basic model dev.

we will also impliment XGboost for a beter feature selection.


## Model Development to understand the feature contribution.

### Linear Regression.
We have built a simple Linear Regression to identify the important features.
this model dose not involve ridge or lasso Regression for the learning adjutment.

for the validation we have implimented the R2 messure.
to find the best R2 we have used the combinations of the features.
the best R2 was 0.93.

The best combination involved all the 5 features left
such as...

    * Stock_Price_Index
    * Consumer_Price_Index
    * Population
    * Mortgage_Rate
    * Real_Disposable_Income

To calculate the importance we have used a different method.
"( coeffecient * standard deviation(coeffecient) )"

which we have also plotted as follows.

![important lin](https://user-images.githubusercontent.com/98254459/209281445-b1742062-b4ea-4ade-a6bb-c1e61f68a6c1.png)

### XGBOOST

This model is an ensemble technique which involves complex calculations to bring the best output.
This model uses the mean to calculate the first set of predictions and then the following model will be (mean - actual).
then the other models will be tuned based on the errors of the previous model.

for this we have set the learning rate to go upto 0.35 runs 35 times.
and also the cross validation was set to 10 fold.

the best score was 0.9950745252231916
The learning rate = 0.22

we also saw that linear Regression had a score of 0.93.

following were the important features from the model.

![xgboost](https://user-images.githubusercontent.com/98254459/209282596-7cc77b8f-f6f4-45fa-869a-d7639d20f6a6.png)

## Conclusion

In this Project, the issue of house price changes and their factors influencing has been adressed original  dataset,  this  project not  only  winsorizes  the 
extreme values in numerical features like ‘stock index price’, but also 
calculates the correlation coefficient and removes the 
highly correlated features a good prediction. They  are 
assessed with a variety of evaluation indicators including 
R2 score and cross-validation score. Among the models, XGBoost outperforms and becomes the selected model because it ranks the first with the cross-validation score. The 
final  model  and  corresponding  essential  factors  are 
subsequently  derived  through  Python  coding. 
From  the  research,  we  obtain  the  following 
conclusions. First, XGboost serves as the best model for 
our house price. It not only gets the highest 
score  in  a  model  assessment  and  makes  a  sensible 
prediction, but also avoids overfitting. Second, the most 
important factors are the consumer price index followed by stock price index and then population.
all the 5 factors are important but still we are making a rank.
we can clearly understand that these 5 factors like Stock_Price_Index, Consumer_Price_Index, Population, Mortgage_Rate, Real_Disposable_Income.
plays major role.