## Image prediction project

## About the project
This project was carried out by gathering three datasets from different data sources having different data formats, assessed the quality and tidiness of the datasets, and then cleaned it to make it analysis ready.

## Data Gathering Steps

- Manually downloadied the WeRateDogs Twitter archive data provided by Udacity and read it into a Pandas dataframe.
- Programmatically downloaded the image prediction data using the Requests library and URL hosted on Udacity's servers.
- Queried the Twitter API for each tweet in the Twitter archive using Python's Tweepy library and save JSON in a text file. Wrote each tweet's JSON data to its own line, then read the tweet_json .txt file line by line into a pandas DataFrame with tweet ID, retweet count, and favorite count.
