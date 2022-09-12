# Instagram Reach Analysis and Prediction

The original content from where the project is based on, you can check the full text here:

https://thecleverprogrammer.com/2022/03/22/instagram-reach-analysis-using-python/

This version is a step by step I've done to understand the original coding and ideas, since the tutorial has some outdated code and some visualizations I didn't like, I've made some changes keeping the answers but rearranging in a better view or recent code. Also, the original code uses plotly to make some graphs, but, despite dinamical, the main goal is to show a result, not to interact with it, at least for now, so plotly will be replaced by seaborn, also due to better arranging visualizations.

The dataset used is based on data gathered from the author's instagram.

Predicting the reach of a certain post is really important for marketing teams, accurate predictions based on recent trends and content help teams to figure out the best strategies to optimize ROI and the target public. The main users of this kind of tool are marketing agencies, which help them to sell ads to companies based on these values.

## Insights from exploratory analysis

- Most traffic of this Instagram account comes from Home, Hashtags, Explore than other sources.

- Most of the content is related to Data Science.

- There is no big difference between Pearson and Spearman correlations, impressions may be modeled by linear algorithms.

- Conversion from visit to follow is 31.2%.

- Dispersion graphs confirmed good linear correlations.

## Model Building and predictions

Three algorithms were tested in order to provide the best model to predict the number of Impressions based on the actions of users, Passive Aggressive Regressor, Least Squares Regression and ElasticNet regressor, all models are implemented on tha Sci-Kit Learn package.

To evaluate the performance of the models builded, two metrics were used, r² determination coefficient and Root Mean Square Error (RMSE), the first as the primary performance indicator and the second for consistency measure, the results are compiled in the table below.

| Metric/Model | PassiveAggressive | ElasticNet | Least Squares |
| :-----: | :------: | :-----: | :-----: |
| r² | 0.923 | 0.828 | 0.802 | 
| RMSE | 760,069.06 |5390.81 | 5505.12 |

## Conclusions

- According to models, Follows and Likes are more likely to describe the reach of a post.

- Original project only uses Passive Aggressive Regressor, but the best performance is given by the ElasticNet.

- ElasticNet uses a mixture of L1 and L2 regularization.

- In an environment where large amounts of data are provided to the models, ElasticNet may underperform and Passive Aggressive Regressor may increase performance.