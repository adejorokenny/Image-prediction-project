## Image prediction project

#### About the project
This project was carried out by gathering three datasets from different data sources having different data formats, assessed the quality and tidiness of the datasets, and then cleaned it to make it analysis ready.

#### Data Gathering Steps

- Manually downloadied the WeRateDogs Twitter archive data provided by Udacity and read it into a Pandas dataframe.
- Programmatically downloaded the image prediction data using the Requests library and URL hosted on Udacity's servers.
- Queried the Twitter API for each tweet in the Twitter archive using Python's Tweepy library and save JSON in a text file. Wrote each tweet's JSON data to its own line, then read the tweet_json .txt file line by line into a pandas DataFrame with tweet ID, retweet count, and favorite count.

#### Quality issues fixed
1. Tweet_id in the three source dataframes has incorrect data type int64 instead of object
2. Some rows have retweet values
3. Expanded_urls column has missing records
4. Expanded_urls column has rows with repeated links
5. Timestamp column has incorrect data type int instead of datetime
6. Timestamp has +0000 which is not relevant
7. Columns in_reply_to_status_id, retweeted_status_id, retweeted_status_user_id, retweeted_status_timestamp, in_reply_to_user_id not needed
8. JPG_URL and IMG_NUM has rows with missing record


#### Tidiness issues fixed
1. Dog stages are in different columns and should be melted into a single column.
2. The three datasets to be merged into a single data set.
3. The columns p1, p2, p3 should form a single column and columns p1_conf, p2_conf, p3_conf should also form single column.

Following the completion of the processes of data gathering, assessing, and cleaning, the datasets were merged to form a single master data file named 'twitter_archive_master.csv'. In addition to the earlier mentioned works done, analysis and visualization was also carried out on the master data and below are some of the insights generated from the analysis.

#### Key insights
1. It was observed that out of all image predictions recorded in the master data, 15.51% of the image predictions of the dataset was predicted wrongly while 84.49% of the dataset have correct predictions. This showed that a major percentage of the dataset had correction image predictions.
2. However, in the analysis and visualization of the year with highest record of tweet, it was also observed that the year with highest number of tweets recorded was 2016 with a total of 971 tweets, followed by year 2015 with a record of 662 and lastly year 2017 with a record of 353.
3. Furthermore, it was also observed that amongst all the tweet_ids recorded in the master data table, tweed_id 744234799360030481 recorded the highest number of favorite count with a total of 144235, while tweet_id 666102155909144576 has the least favorite count with a total of 66.  Finally, in the master data table, it was also observed that the tweet_id 749981277374128128 has the highest rating numerator with a rating total of 1776 while we have two tweet_ids (835152434251116546 and 746906459439529985) with zero (0) rating numerator.
