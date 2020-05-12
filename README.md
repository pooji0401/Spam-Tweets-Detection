# Spam Detection in Twitter

The aim of the project is to classify spam tweets based on Twitter Account and Content based features on twitter handles.

A labelled dataset of Spam Tweets was obtained from Reddit, making supervised learning possible. This was an imbalanced dataset, containing a majority of Non-spam tweets. Therefore, a subset of this dataset was used to develop the model.

After tuning the model, using cross validation techniques, the best performance was obtained using Naive Bayes Model, using the text based features alone. 

In the later phase of the project, an ensemble model- Voting Classifier using combination of both account based and text based features was developed which yeilded the best performance.

## DATA UNDERSTANDING AND PREPARATION

### Data Extraction
Due to data streaming limitations imposed by Twitter API, we obtained data from external sources. A dataset containing Tweet IDs and labels(spam/ham) was taken from Reddit Datasets for our analysis. This dataset was contributed by PLOS one journal. The tweet IDs were extracted from Twitter API using Social Feed Manager. These tweet IDs were scraped using GET statuses/ user_timeline method or the POST statuses/ filter method of the Twitter Stream API. These tweet IDs were in-turn used to extract the respective tweet attributes using Hydrator – a publicly available application that is used to turn the Twitter IDs into Twitter JSON. This JSON file was later converted into a CSV file for data processing. 

Finally, the extracted dataset has two files. One of the files contains tweet information for the corresponding tweet IDs. This file, extracted from Hydrator, contains tweet attributes – including the all the account- based features. The second file also contains tweet ID along with the labels - 1 for spam and 0 for ham.  These files were merged using the common attribute - Tweet ID, in order to map the tweets with their respective features.

### Balancing Data Set
The final dataset, after hydrating, contains 66,610 tweets in total. Of these, there were 4457 spam tweets and 62153 ham tweets. This clearly indicates that the data set is highly unbalanced. This imbalance in data might lead to a high bias and such classification will generally follow a majority rule. Therefore, the dataset was balanced by randomly sampling same number of ham tweets as spam tweets.

