# IBM Advanced Data Science Specialisation - powered by Coursera
Advanced Data Science Capstone Repo

# Political Data Science
Analysing Sentiment towards a new Scottish Independence Referendum

### Table of Contents

1. [Installation](#installation)
2. [Project Motivation](#motivation)
3. [File Descriptions](#files)
4. [Results](#results)
5. [Licensing, Authors, and Acknowledgements](#licensing)

## Installation <a name="installation"></a>

All necesary libraries are indicated at the beggining of each notebook:
  - [ETL](ETL_Sentiment_Analysis_Scotref2.ipynb).  
  - [Feature Engineering](Feature_Engineering_Sentiment_Analysis_Scotref2.ipynb)
  - [Model Definition and Training](Models_Definition_&_Training_Sentiment_Analysis_Scotref2.ipynb)
  - [Model Evaluation](Model_Evaluation_Sentiment_Analysis_Scotref2.ipynb)
  - [Model Deployment](Model_Deployment_Sentiment_Analysis_Scotref2.ipynb)

The code should run with no issues using Python versions 3.*.

## Project Motivation<a name="motivation"></a>

<p align=justify>
The role of social media in shaping politics these days is hard to deny and Twitter is arguably the most studied and used source of data even though in many countries Twitter is not the main player. We use mostly Twitter data because that's what's (almost) publicly available whereas it’s (almost) impossible to collect any useful data from Facebook. As part of the IBM Advanced Data Science Specialisation, I chose to look into the current political situation in Scotland after the Brexit vote, and most recently, Boris Johnson's win the winter General Election of 2019.</p>

<p align=justify>
Scottish voters were first asked whether they wanted Scotland to become an independent country in a referendum in September 2014; the result was 55% to 45% against independence. In its manifesto for the 2016 Scottish Parliament elections, the Scottish National Party (SNP) argued that “Scotland being taken out of the EU against our will” would justify a second vote on independence. Scotland voted by 62% to 38% in favour of Remain in the EU referendum in June 2016, and First Minister Nicola Sturgeon concluded that indyref2 “must be on the table”. In March 2017 Sturgeon formally requested the consent of Westminster to hold another referendum. But Prime Minister Theresa May declined, arguing that “now is not the time”. The first minister renewed calls for a second vote in April 2019, announcing a new process for deciding Scotland’s constitutional future. The SNP's 2019 General Election manifesto stated that the party intended to hold a second referendum in 2020; and they won 48 of Scotland’s 59 seats. So, naturally, Nicola Sturgeon has now claimed there is a “renewed, refreshed and strengthened mandate” for another vote.She has formally request the power to hold an independence referendum before the end of 2020, but it has been denied by Boris Johnson. All of this has created a complicated environment in a nation that appears to be in a very difficult (and not very favourable) position within Boris Johnson's UK.</p>

<p align=justify>
This project looks into Twitter as political barometer for Scottish Independence using Sentiment Analysis, a Natural Language Processing subfield. I downloaded the dataset using twitter’s API. A week of Tweets were scrapped from 2020-01-08 13:49:18 to 2020-01-15 20:02:23 using keywords "indyref2", "scottish independence" and "scotref". The process I used to scrape the data and to analyze sentiment can be repeated for any twitter account of media page.</p>


## File Descriptions <a name="files"></a>

  - [ETL](ETL_Sentiment_Analysis_Scotref2.ipynb).  Notebook for exploratory data analysis and insights for feature extraction. 
  - [Feature Engineering](Feature_Engineering_Sentiment_Analysis_Scotref2.ipynb)  Feature extraction based using polarity scores and POS count. 
  - [Model Definition and Training](Models_Definition_&_Training_Sentiment_Analysis_Scotref2.ipynb) Pipeline to train Supervised Machine Learning models (Naive Bayes and Support Vector Machine classifiers) using Scikit-Learn; and Deep Learning Models (LSTM Recurrent Neural Network and LSTM with regularisation) using Keras. 
  - [Model Evaluation](Model_Evaluation_Sentiment_Analysis_Scotref2.ipynb) Exploration of metrics (Confusion Matrices, F1-Score, Recall, Precision and Accuracy) to check model performance.
  - Model Deployment - In construction : Sentiment analysis with twitter data, geoplots for storytelling.

## Results<a name="results"></a>

After training and testing, the performance of the LSTM network was found to be better than other models and is the one we used for model deployment. We chose LSTM over the SVM model because generally, deep learning really shines when it comes to complex problems such as natural language processing. Another advantage is that you have we worry less about the feature engineering part when it comes to model deployment.

Ultimately the true test was testing the model on unseen, real world data.

We predicted sentiment scores (positive/negative) on the tweets data set. We found that tweets from cities in Scotland have an overall more negative sentiment than those from England and Wales. We observe one city in Northern Ireland with overall neutral sentiment. The city with the highest negative sentiment overall (-19) is Glasgow, followed by Invergordon (-13). We also found that a lot of tweets originate from high population density urban areas, as expected. These areas are Glasgow, Edinburgh, London, Liverpool, Manchester and Cardiff.

Again, this does not mean that tweets from Scotland have a negative attitude towards Scottish Inpendence but rather the tweets carry a negative sentiment, for example they can be interpreted as angry tweets. The same can be said with tweets with positive sentiment from  English cities. 

For our next steps, we identify that stakeholders maybe interested in the specific emotions towards Scottish Independence rather than the polarity itself. They may want to understand how people feel about the topic, or recognizing growing anger or fear associated with it. It would be an interesting future project to re-train a classifier to learn and predict emotion, such as affection, anger/rage, fear/anxiety, joy or sadness/dissapointment.

## Licensing, Authors, Acknowledgements<a name="licensing"></a>

Acknowledgements to source-code are made throughout the notebooks. Feel free to use the code here as you would like! 
