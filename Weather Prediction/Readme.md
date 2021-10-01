# Weather Prediction 

### [The Rain in Australia Dataset](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) is from kaggle which contains 145460 days of weather reported in 49 different places . We need to predict if it will rain the next day.

### Things Done
-----

- Data Analysis Using 
    - Matplotlib
    - seaborn
    - plotly (A high level and a powerful API for Data visualisation 
- A model to make Prediction using scikit learn
> Initially used `sklearn.linear_model` . Performed quite bad. 
> Prediction on a day it rained had a prob of 52% only
> Results:-
> - Validation Accuracy : 84.1 %   


> Then used `sklearn.tree` (**RandomForests** and **Decison Trees**) . Performed quite bad. 
> Though validation accuracy remained almost same . The performance on real world datasets were much better
> Results:-
> - Validation Accuracy : 85.21 %  


