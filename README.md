# Spam-Tweets-Detection
In this project, we are performing a supervised learning task - Classification of tweets using Twitter Account based
features & Content based features. 

From business perspective, the main objective of Twitter is to reduce False Positives as they should not delete legitimate
Twitter handles and tweets. In this case a False Positive occurs when a Non Spam Tweet i.e. a Ham tweet is misclassified as a Spam Tweet. 
At the same time, classifying an account/tweet as SPAM is also very important. Therefore, the main objectives were to reduce the False Positive Rate at the same time increase the accuracy.

A labelled dataset of Spam Tweets was obtained from Reddit, making supervised learning possible. This was an imbalanced dataset, containing a majority of HAM tweets. Therefore, a subset of this dataset was used to develop the model. 

Significant features were identified and developed as a part of feature engineering process.

For the Model Selection, Models were developed using Account Based Features including User Favoourite count, Number of Followers, Number of people whom the user is following, etc. 
Models were also developed using content based features such as polarity score, objectivity score, length of the tweet, etc. 

After tuning the model, using cross validation techniques, the best performance was obtained using Naive Bayes Model, using the text based features alone. 

In the later phase of the project, an ensemble model- Voting Classifier using combination of both account based and text based features was developed which yeilded the best performance.
