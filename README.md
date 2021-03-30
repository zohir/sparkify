# sparkify

This article documents my Capstone project of the Data Science nanodegree with Udacity.com.  
I have chosen specifically this project because it should have reconciliated my new knowledge on data science with python with my background on Bigdata with Scala and Spark on AWS.  

The project is documented in a blog post on Medium
https://medium.com/@zohir.elkhattabi/customer-churn-with-local-pyspark-ba462a89ff5f

  
## Project Overview & problem statement
Sparkify is a music platform that wants to reduce the churn of their paying users by executing targeted marketing campaigns. Their marketing team needs recurrently to identify customers with a high probability to leave their service or to downgrade to the free package. 
  
To do that Sparkify, we received two months of user’s logs. The logs include the obvious music’s requests actions, the downgrade requests and other logs of actions like the Login, Help, feedbacks on music, requests to add friend...      

The Project will consist in discovering the behavior that could forecast the churn probability of paying users in the next days or weeks. The project will result in  a model that could be executed each week, to detect next week’s churns.  

I have defined a two-weeks observation period at the end of the two months data. This will simulate that we only have 6 weeks of data and that we have to predict.  the users that will churn during the last two-weeks.  
The models features will only include data from the first 6 weeks of the dataset.   
The model label-churn will only be based on the last two-weeks of evaluation. 


# Results:
The Gradient-boosted Tree was the most promising and give a score of 0.89939.  
Tunning the model on hyper parameters like maxDepth, maxIter, maxBins, minInstancesPerNode with cross validation fold of 5 did not give a better result.  



# Files:  
|-- Sparkify.  
  |-- step-1-load-dataset-and-explore.ipynb - jupyter notebook to load, clean and ML feaures engineering. 
  |-- step-2-detect-churn.ipynb             - jupyter notebook to train and evaluate the ML model. 
  |-- README.md. 
  
  
# Libraries:  
python=3.6.12. 
numpy=1.12.1. 
pandas=0.23.3. 
plotly=4.14.3. 
spark=3.1.1. 

