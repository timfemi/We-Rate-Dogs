# We-Rate-Dogs Data Wrangling Project

## Introduction
This project was one of the projects in Udacity Data Analyst Nanodegree program. It is primarily focused on wrangling Data from a twitter user, [WeRateDogs](https://twitter.com/dog_rates) account using Python. The project is done in a Jupyter Notebook (`wrangle_act.ipynb`). Dogs are rated on this user's twitter account with entertaining tweets and analysis.

## Project Breakdown
For this project, I considered only tweets (no retweets). I also noticed that not all of the original tweets in the dataset are dog ratings and some are retweets.

Fully assessing and cleaning the entire dataset would require much effort, I only looked into a subset of its issues - twelve quality issues and two tidiness issues.

The tasks for this project are broken down into:
- Data wrangling, which consisted of:
  > Data gathering
  
  > Assessing data
  
  > Cleaning data
  
  > Storing, analyzing, and visualizing the wrangled data
  
- Reporting on my data analyses and visualizations (act_report.pdf)

## The Data and Analysis.
WeRateDogs provided their Twitter archive of tweets, which contains (tweet ID, timestamp, text, etc.) to be used in this project. 

The project includes three datasets, the first dataset was a csv, (`twitter-archive-enhanced.csv`) provided by Udacity that required manual downloading, the second dataset was a tab separated value text hosted on Udacty's servers which was downloaded programmatically using the `Requests` library. The final data was gotten using twitter API. 
In using the `tweet_ids` in the first dataset I queried the API for each tweets JSON data using the python's `Tweepy` library and stored each entire set of json data in a file called `tweet_json.txt` file. <br>
The dog stages (doggo, floofer, pupper, and puppo) were summarised into one column. This shows the dog's growth development stage as at the time of the tweet. These columns needed to be assessed and cleaned as the extraction process from the twitter server wasn't perfect. This was due to some tweets which has been deleted by the user.

I cleaned the data set using the quality and tidiness issues which I found and made some analysis on the Dog breeds which has the most likes and ratings.
