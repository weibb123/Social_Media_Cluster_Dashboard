# Social_Media_Cluster_Dashboard
![image](https://github.com/weibb123/Social_Media_Cluster_Dashboard/assets/84426364/54bb417e-51da-486f-b004-d1c8cd07e5e5)

##### Table of Contents
[Problem](#Problem)

[EDA](#EDA)  

[Method](#Method)

[Evaluation Metrics](#Evaluation)

[Hypothesis Testing](#Hypothesis)

[Dashboard](#dashboard)

[Actknowledgement](#Actknowledgement)


## Problem
Suppose customers come and ask to help with social media analytic projects to help manage social media for their clients.\
They want to quantify what is working and what is not.\
Problem Solved: Create clusters of social media posts and identify high performance posts for customers to see what they do uniquely to help drive performances.

## EDA
Reviewing the data quality, cleansing the data, and checking features are good to feed in model and split into train-test set.\
![image](https://github.com/weibb123/Social_Media_Cluster_Dashboard/assets/84426364/14401496-9c4c-4686-8d91-22d5c4a8a12a)\
Shorts are common type of posts. Tiktok, instagram reels, and youtube shorts are popular since they are easy to produce and grab audience attentions.\
![image](https://github.com/weibb123/Social_Media_Cluster_Dashboard/assets/84426364/15aa353d-cdfe-4ad5-8e8c-5c3da4eb36ca)\
Note: Dark bar refers to the confidence interval of where the true average lies in..\
Video and shorts are fairly consistent to perform well whereas the performance of photos and texts might vary in real world.


## Method
Use KMeans as a choice to create cluster since the problem is an unsupervised learning. Before feeding features into the model, I need to convert OBJECT columns into numeric through one-hot encoding and standarize the numeric columns for mean of 0 and variance of 1 for better clustering performance.

## Evaluation
To identify the best number of clusters to create, we would use the Elbow method.\
![image](https://github.com/weibb123/Social_Media_Cluster_Dashboard/assets/84426364/63f25e28-894e-4bc0-aa2a-04cff7afe039)\
ZOOM IN VERSION\
![image](https://github.com/weibb123/Social_Media_Cluster_Dashboard/assets/84426364/5ad3bb5b-552e-4040-8e2e-a425f4e00345)\
We can see that the best clusters to choose is four.

## Hypothesis
Using the clusters we created with KMeans, we can perform a hypothesis test to validate our hypothesis.\
\
![image](https://github.com/weibb123/Social_Media_Cluster_Dashboard/assets/84426364/00040453-87f3-4d41-aa29-852d24a87490)\
Based on the clusters, we see that cluster 1 have a higher number of reactions and comments than other three clusters.

We want to test if cluster 1 have a higher number of reactions on average

Null hypothsis: number of reactions of cluster 1 is less than or equal to other clusters\
Alternative hypothsis: number of reactions of cluster 1 is greater than other clusters.\
Using a t-test, we find that p-value < 0.01, which suggests us to reject null hypothesis since it is unlikely to see the observed data occur if null hypothesis is true.
\
Next, with this results and the hypothesis confirmed, we can inform others to look into cluster 1 to seek engagement.

## Dashboard
The end result of this project is to create an interactive dashboard with DASH.

## Actknowledgement
Thanks to Nicholas Renotte for providing the dataset!
