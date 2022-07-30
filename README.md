# We-Rate-Dogs Data Wrangling Project

## Introduction
This project was one of the projects in Udacity Data Analyst Nanodegree program. It is primarily focused on wrangling Data from a twitter user, [WeRateDogs](https://twitter.com/dog_rates) account using Python. The project is done in a Jupyter Notebook `wrangle_act.ipynb`. Dogs are rated on this user's twitter account with entertaining tweets and analysis.

## Project Details
For this project, I considered only tweets (no retweets). I also noticed that not all of the original tweets in the dataset are dog ratings and some are retweets.

Fully assessing and cleaning the entire dataset would require much effort, I only looked into a subset of its issues - twelve quality issues and two tidiness issues.

The tasks for this project are broken down into:
- Data wrangling, which consisted of:
  > Gathering data
  
  > Assessing data
  
  > Cleaning data
  
  > Storing, analyzing, and visualizing the wrangled data
  
- Reporting on my data analyses and visualizations (act_report.pdf)

## The Data and Analysis.
WeRateDogs provided their Twitter archive of basic tweet data (tweet ID, timestamp, text, etc.) for use on this project. The "enhanced" csv file (twitter_archive_enhanced.csv) also contains columns which were extracted programatically: the rating numerator, rating denominator, dog's name, and dog stages (doggo, floofer, pupper, and puppo) were summarised into one column as this shows the dog's growth development stage as at the time of the tweet. These columns needed to be assessed and cleaned as the extraction process from the twitter server wasn't perfect. This was due to some tweets which has been deleted by the user.

I used the tweet IDs to query the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt. I then read the txt file line by line into a pandas DataFrame only including the desired variables; retweet count and favorite count.

Udacity also provided a link to image_predictions.tsv which was downloaded programatically using the Requests library.

I cleaned the data set using the quality and tidiness issues which I found and made some analysis on the Dog breeds which has the most likes and ratings.
