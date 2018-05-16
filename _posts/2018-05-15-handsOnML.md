---
layout: post
title: "Hands on ML with Scikit-Learn & TensorFlow"
---

## Challenges in Machine Learning.
#### Insufficient quantity of training data.
If the training data is not covering all the classes or is not exhaustive then the models do not learn appropriately. 
Even simple models can perform at par with complex models given appropriate amount of data. 
#### Biased data.
If the training data is not representative then the learning is limited. 



## Interesting data sets
### Popular repositories
 * UC Irvine Machine Learning Repository
 * Kaggle datasets
 * Amazon’s AWS datasets
 * http://dataportals.org/
 * http://opendatamonitor.eu/
 * http://quandl.com/
 * [Wikipedia’s list of Machine Learning datasets](https://en.wikipedia.org/wiki/List_of_datasets_for_machine_learning_research)
 * [Quora.com question](https://www.quora.com/Where-can-I-find-large-datasets-open-to-the-public)
 * [Datasets subreddit](https://www.reddit.com/r/datasets)


# Machine Learning Project Checklist. 

## Looking at the Big Picture.
### Frame the problem
Ask  questions about the problem to realize.
  * What exactly is the business problem that will be solved. 
  * What is the current solution that is being used if on exists ? 
    * You shall figure out a way to improve the present solution by using data and models. 
  * Decide on the details of the solution such as, type of learning, batch/online training etc. 
### Select a Performance Measure
Know about the basic loss functions that are generally used. 
RMSE and Mean absolute error are used generally to formulate the loss functions. 
RMSE neglects small errors and is sensistive to outliers, but where the outliers are rare RMSE is good. 
### Check the assuptions
Validate and verify the assumtpions made in arriving at the solution. 

## Get the data. 
Try writing functions that would download and place datasets with unzipping etc so that it will be easy going forward.
Get to know the data by using pandas's function such as .info(), .describe(), .hist(), .head() etc. 
Make sure you have already sampled a stratified test set sample before you analyze the whole data.(data snooping bias).

### Sampling
Sampling is quite important as random sampling into train and test sets could lead to overfitting to the whole data. 
To improve the quality of test/train splitting use stratitfied sampling.
* Use a feature that is determinental and obtain categories of instances based on its values.
* use something like StratifiedShufflesSplit to obtain stratified samples.
* make sure you use random_state to generate consistent splits. 

## Discover and Visualize the data

Try making up basic visualizations based on initial intuitions and combinations of different features.
Learn and use statistical tools to determine important features. 


## Data preperation



## Important sklearn libary function. 
### Data
* from sklearn.model_selection import train_test_split
  * train_set,test_set=train_test_split(data,test_size=0.2, random_state=42)
  * random_state is a seed to control the randomness. 
* 

## To learn
* Different sampling techniques
* Visualization techniques. Search for a course on lynda.com
* Learn and use statistical tools to determine important features. 





  
