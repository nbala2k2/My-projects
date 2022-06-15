# Weather Prediction 

The Rain in Australia [Dataset](https://www.kaggle.com/jsphyg/weather-dataset-rattle-package) is from kaggle which contains 145460 days of weather reported in 49 different places . We need to predict if it will rain the next day.

## Summary

### 1. Performed a EDA to understand which features are important ( simple graphical interpretations )
        
      -  Used libraries: Matplotlib | Seaborn | Plotly | scikit-learn (for models)


### 2. A simple model to make Prediction using scikit learn . [Link to Notebook](https://github.com/nbala2k2/My-projects/blob/main/Weather%20Prediction/weather.ipynb)
    
      - Initially used `sklearn.linear_model` . Performed quite bad. 
      - Prediction on a day it rained had a prob of 52% only
      - Results:- 
      
           > - Validation Accuracy : 82.41 %
           > - Test Accuracy       : 81.24%  


### 3. Improved by using `sklearn.tree` (RandomForests and Decison Trees) . [Link to Notebook](https://github.com/nbala2k2/My-projects/blob/main/Weather%20Prediction/weather_DecisionTrees%20and%20Random%20Forests.ipynb)
    
      - The "performance improved drastically" (explained in detail in next point after results). 
      - Results:- 
      
           > - Validation Accuracy : 85.37 %
           > - Test Accuracy       : 84.26 % 
      
      - **The accuracy has not changed much , Then how is the performance said to be improving can be a nice question.**
            
              > A day when it rained was taken and the probability that it rains was obatined from our trained models. 
              > It's obvious that a good model would give a higher probability in predicting it rained.
              > The same was observed the linear sklearn classifier gave only 52% ,
              > But our decision trees and random forest model gave about 93% probability that it will rain
              > This clearly shows the performace has improved drastically.
              
### 4. `Gradient boosting model (Xgboost)` was also tested [Link to notebook](https://github.com/nbala2k2/My-projects/blob/main/Weather%20Prediction/Weather_GBM.ipynb)
      - It performed better than  sklearn linear model but not as good as our decison trees and random forest models.
      - Results:- 
      
           > - Validation Accuracy : 85.53 %  
           > - Test Accuracy       : 84.16 %
      - Its probability of predicting that it rains or a specified day (same day as above) was **84.48 %**.

## Conclusion

        > GBM's and the tree models seem to give a higher accuracy as compared to a linear model which is as expected cause of model 
    complexity and computation power. 
        > Among GBM's and tree models its better we go with tree models as they took computationally less time and also seem to predict 
    days it rains with higher probability
