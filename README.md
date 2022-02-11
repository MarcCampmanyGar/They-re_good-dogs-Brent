# They're good dogs Brent
[https://knowyourmeme.com/memes/theyre-good-dogs-brent]

Data wrangling exercise from twitter's "WeRateDogs" account.

## Tools

- Jupyter Notebook
- tweepy API for scrapping twitter
- Requests library

## Files to gather
- The WeRateDogs Twitter archive. File provided: (twitter_archive_enhanced.csv)

- The tweet image predictions, i.e., what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) is hosted on Udacity's servers and should be downloaded programmatically using the Requests library and the following URL: https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv

- Each tweet's retweet count and favorite ("like") count at minimum, and any additional data you find interesting. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called tweet_json.txt file. Each tweet's JSON data should be written to its own line. Then read this .txt file line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count. Note: do not include your Twitter API keys, secrets, and tokens in your project submission.

## Key points to keep in mind when data wrangling for this project:

- You only want _**original ratings (no retweets) that have images**_. Though there are 5000+ tweets in the dataset, not all are dog ratings and some are retweets.
- Assessing and cleaning the entire dataset completely would require a lot of time, and is not necessary to practice and demonstrate your skills in data wrangling. Therefore, the requirements of this project are only to _**assess and clean at least 8 quality issues and at least 2 tidiness issues**_ in this dataset.
- Cleaning includes merging individual pieces of data according to the rules of tidy data.
- The fact that the rating numerators are greater than the denominators does not need to be cleaned. This unique rating system is a big part of the popularity of WeRateDogs.
- You do _**not need to gather the tweets beyond August 1st, 2017.**_ You can, but note that you won't be able to gather the image predictions for these tweets since you don't have access to the algorithm used.

## Deliverables:
1) Store the clean DataFrame(s) in a CSV file with the main one named _**<u>twitter_archive_master.csv.<u>**_ If additional files exist because multiple tables are required for tidiness, name these files appropriately. Additionally, you may store the cleaned data in a _**<u>SQLite database<u>**_.

2) Analyze and visualize your wrangled data in your _**<u>wrangle_act.ipynb<u>**_ Jupyter Notebook. **At least three (3) insights and one (1) visualization must be produced.**

3) Report called _**<u>wrangle_report.pdf<u>**_ or _**<u>wrangle_report.html<u>**_ that briefly describes your wrangling efforts. This is to be framed as an internal document.

4) Written report called _**<u>act_report.pdf<u>**_ or _**<u>act_report.html<u>**_ that communicates the insights and displays the visualization(s) produced from your wrangled data. This is to be framed as an external document, like a blog post or magazine article, for example.
