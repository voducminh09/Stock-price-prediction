# Introduction

<img src = "image/Stock1.jpg" width = "620" height = "300">

Every stock market investor knows the pain of stock fluctuation, since predicting the stock market's direction is one of the hardest thing to do. There are many factors involved, from overall economy performance or company's fundamentals to news catalysts or market makers' manipulation. As an investor, I am interested to figure out if Machine Learning algorithms have the potential to unearth patterns in the stock market that human cannot detect, which can be used to improve the accuracy of stock prediction. In this project, I perform stock price prediction by applying Machine Learning algorithms on historical data of Apple and Dow Jones Industrial Average.


## Apple stock price prediction

### Decision Tree
<img src = "image/Apple Decision Tree.PNG" width = "600" height = "360">
MEA for best max_leaf_nodes: 10.490951367026877

### Random Forest
<img src = "image/Apple Random Forest.png" width = "600" height = "360">
MAE for Random Forest Model: 10.508806363636364

Decision Tree and Random Forest can make solid predictions. However, they cannot predict the stock prices in validating dataset that are higher than the maximun stock price in training dataset.

### k-nearest Neighbors
<img src = "image/Apple K-nearest neighbor.png" width = "600" height = "360">
MAE for k-nearest Neighbor Model: 42.37149350649351

k-nearest neighbors predict the fluctuation well. But it detects a falling partern and then predict the valiadation data with huge Mean Absolute Error, so it does not work really well with this dataset.

### Prophet
<img src = "image/Apple Prophet.png" width = "600" height = "360">
MAE for Prophet Neighbor Model: 13.589607214894048

### ARIMA
<img src = "image/Apple ARIMA.png" width = "600" height = "360">
MAE for ARIMA Model: 11.078197046913763

## Dow Jones index price prediction

### Decision Tree
<img src = "image/Dow Decision Tree.png" width = "600" height = "360">
MEA for best max_leaf_nodes:212.06950820547277

### Random Forest
<img src = "image/Dow Random Forest.png" width = "600" height = "360">
MAE for Random Forest Model: 189.0973996753243

So, with stock (or index) prices where validation prices are not higher than the maximum price in training dataset, Decision Tree and Random Forest prediction is really powerful!

### k-nearest Neighbors
<img src = "image/Dow K-nearest neighbor.png" width = "600" height = "360">
MAE for k-nearest Neighbor Model: 1203.5057244155848

k-nearest neighbors fits Dow Jones dataset much more than Apple dataset.

### Prophet
<img src = "image/Dow Prophet.png" width = "600" height = "360">
MAE for Prophet Neighbor Model: 4222.767106506855

### ARIMA
<img src = "image/Dow ARIMA.png" width = "600" height = "360">
MAE for ARIMA Model: 3258.3506585789373

However, as mentioned in the beginning, keep in mind that stock (or index) prices are affected by news about the market or the company and by the company's fundamentals, so there are still a lot of possible factors that are not accounted for in this model.
