# Spam-Tweets-Detection

The aim of the project is to classify spam tweets based on Twitter Account and Content based features on twitter handles.

A labelled dataset of Spam Tweets was obtained from Reddit, making supervised learning possible. This was an imbalanced dataset, containing a majority of Non-spam tweets. Therefore, a subset of this dataset was used to develop the model.

After tuning the model, using cross validation techniques, the best performance was obtained using Naive Bayes Model, using the text based features alone. 

In the later phase of the project, an ensemble model- Voting Classifier using combination of both account based and text based features was developed which yeilded the best performance.
