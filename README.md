# Real Estate Price Prediction - Random Forest (via scikit-learn)

## Approach:

- load Pandas DataFrame containing (Dec-17) housing data
- do some simple data exploration / visualisation
- remove non-numeric data, NaNs, and outliers
- split the data in train and test sets (+ normalise independent variables where required) 
- find the optimal model parameters using [scikit-learn](http://scikit-learn.org/stable/)'s GridSearchCV
- fit the model using GridSearchCV's optimal parameters
- evaluate estimator performance by means of 'shuffled' nested cross-validation
- predict cross validated estimates of y for each data point

## Packages required

- [Python 3.7.0](https://www.python.org/downloads/)
- [Matplotlib](https://matplotlib.org/)
- [Pandas](https://pandas.pydata.org/)
- [Numpy](https://docs.scipy.org/doc/)
- [scikit-learn](http://scikit-learn.org/stable/)



## Scores (nested 'shuffled'cross-validation - Rsquared)

**1. Random Forest Regression**        									                                   
  * Score:  0.839
### Sample data input (Pandas DataFrame)
```
	CRIM	ZN	INDUS	CHAS	NOX	RM	AGE	DIS	RAD	TAX	PTRATIO	B	LSTAT	MEDV
0	0.00632	18.0	2.31	0	0.538	6.575	65.2	4.0900	1	296	15.3	396.90	4.98	24.0
1	0.02731	0.0	7.07	0	0.469	6.421	78.9	4.9671	2	242	17.8	396.90	9.14	21.6
2	0.02729	0.0	7.07	0	0.469	7.185	61.1	4.9671	2	242	17.8	392.83	4.03	34.7
3	0.03237	0.0	2.18	0	0.458	6.998	45.8	6.0622	3	222	18.7	394.63	2.94	33.4
4	0.06905	0.0	2.18	0	0.458	7.147	54.2	6.0622	3	222	18.7	396.90	5.33	36.2
 
 ``` 
 
