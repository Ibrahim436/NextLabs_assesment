# NextLabs_assesment
All the solutions for the problem statements given here

#### Problem (1) - part 1

Regex to match the given string : {"orders":[{"id":1},{"id":2},{"id":3},{"id":4},{"id":5},{"id":6},{"id":7},{"id":8},{"id":9},{"id":10},{"id":11},{"id":648},{"id":649},{"id":650},{"id":651},{"id":652},{"id":653}],"errors":[{"code":3,"message":"[PHP Warning #2] count(): Parameter must be an array or an object that implements Countable (153)"}]}

Please find the regex from the folder regex in this repo

#### Problem (1) - part 2

Here is the link to the repository of the chrome reviews-ratings mismatch identifier : https://github.com/Ibrahim436/review_rating_mismatch_identifier

Trained a BERT sentiment classifier model for this application : https://colab.research.google.com/drive/1RtDjTsGCX9uanlgFmNv2ITjsXZQ-PKsT?usp=sharing

Application demo is present in the video link given above .

  ######## Deployment challenges
  1) I tried deploying using Heroku. While deploying the model file (around 412 MB) was getting corrupted which was failing the code. Heroku does some sort of commpression which is causing the problem. It does not support Git LFS. I had to use git LFS to commit code with model (file size more than 100 MB).
  2) AWS Beanstalk was also tried, which gave out a memory error while trying to deploy.

#### Problem (1) - part 3

Please refer the folder Ranking-problem in this repo : there .ipynb  of the notebook which explains the solution.

1. Is there any co-relation between short description, long description and ranking? Does the placement of keyword (for example - using a keyword in the first 10 words - have any co-relation with the ranking)? -->More the number of keywords within first 15 words of discription lesser is the quantitative value of rank (which means high rank in reality). keyword in short description barely had a relationship with rank alone but it represented a correlation when they were combined with long discription for obvious reasons.
2. Does APP ID (Also known as package name) play any role in ranking? There is no relationship between appid , rank and keyword . keyword present in app id does not give higher ranks. But I found the API IDs distributions which respresented the most popular or highly ranked apps and the least popular and ranked apps.

#### Problem (2) - part 1

Grammar check : Used a pretrained model GPT-2 which showed decent results. The notebook file and result csv file is present in Grammar-check folder.
Used a scoring schema for the grammar correctness as well which ranges from 0-100.

#### Problem (2) - part 2

1) At my previous company we had a client who came up with address matching problem. The problem was to match the raw input addresses coming from the users to the actual addresses of an institution in the united states. This problem is the most challenging one which I have faced. We put forward several number of POCs accross various methods and services such as Placekey.io,google place API. Currently the service which is at use is doing only like 60-70 percent of the job. We increased it by another 15 percent by bringing in a deep matcher model to the pipeline. The most challenging part was the feature engineering of the current dataset which we were given with for the training of the model. Dataset was over 2 million records from the database but that itself had several scrappy standardized addresses.We had to apply sever cleaning logics using SQL queries and python which improved the model performance at the end. 

2) option D : The set of pairs (a, b) for all non-negative real a,b

