# App Review Sentiment Analysis (GoPay)
## Business Understanding
User reviews are important for an app, by understanding the sentiment of user reviews we can know whether users are satisfied with the app or not, so we know when the app needs to be improved. But it would be very resource-intensive to handle a lot of user reviews by classifying them ourselves. Machine learning models can be a solution to help classify them automatically.

## The Objectives
The aim of this project is to create a sentiment classification model based on reviews. As a result, this model can help companies to know whether user reviews have positive or negative sentiment, so that they know whether their features and services need to be improved or maintained.

- Collect and process the user review data of GoPay app.
- Perform sentiment analysis to classify the user reviews into positive, negative, or neutral.
- Build an accurate predictive model to predict the user sentiment based on their review text.

## Data Understanding
The data obtained through scraping technique of user review data for GoPay app on Google Playstore with (google play scraper)[https://pypi.org/project/google-play-scraper/] library. [Dataset](https://github.com/MuhamadSyarifFakhrezi/sentiment-analysis/blob/main/gopay_reviews.csv)

## Text preprocessing
Text preprocessing techniques indclude: 
- Text cleaning (remove mentions, hashtags, links, digits, and punctuations).
- Lower case.
- Tokenizing.
- Remove stopwords.
- Stemming.
- Remove slangwords.

![Screenshot (988)](https://github.com/user-attachments/assets/327184a3-13e9-406b-9ab0-0b3551242f94)

## Labelling
Labelling process is done based on the user review, each word in the text of user review checked and given a score based on a dictionary of [positive](https://github.com/angelmetanosaa/dataset/blob/main/lexicon_positive.csv) and [negative](https://github.com/angelmetanosaa/dataset/blob/main/lexicon_negative.csv) words, then the total score used as a reference to determine whether the text belongs to the positive, negative, or neutral sentiment category.

![distribution chart](https://github.com/user-attachments/assets/d5f85dc3-a34a-41c3-adec-91b3b9cc9666)

![text lenght distribution](https://github.com/user-attachments/assets/50354c69-7702-489c-9f9b-4187bf6da856)

![most frequent words](https://github.com/user-attachments/assets/e9a50468-ea38-4332-8b47-1d9e175ac462)

As we can see, majority of the user reviews have positive sentiment followed by negative and neutral sentiment. The average text length ranges from 1-10 words. And the top three most frequently occuring words are 'mantap', 'bagus', and 'bantu'.

### Word Cloud
![positive word cloud](https://github.com/user-attachments/assets/1b9c3910-d319-47c4-a8c2-82525ba2bb53)

![neutral word cloud](https://github.com/user-attachments/assets/6e914e2d-e914-43da-af03-ba7b868ebd13)

![negative word cloud](https://github.com/user-attachments/assets/4d7aa94b-e05b-450c-8910-922af1379f47)

## Feature Extraction
The feature extraction used is TF-IDF (Term Frequency-Inverse Document Frequency).

## Modeling
Four models with different algorithms were compared to find the model with the best perfomance, the four algorithms are Naive Bayes, Random Forest, Logistic Regression, and Decision Tree.

## Evaluation
Of the four models, the logistic regression model has the best accuracy compared to other models, with 91% accuracy.

![Screenshot (987)](https://github.com/user-attachments/assets/eb5b96ea-977d-4d7b-ae54-fb092c7a3842)

![confusion matrix](https://github.com/user-attachments/assets/0dc90fb1-f281-4b2b-85ef-080ff894143c)

## Conclusion
- Based on data analysis, the GoPay app has mostly positive sentiment (around 48% of the total data), the most frequently occuring words are also mostly positive words, this shows that the average user of GoPay app is satisfied with features and services provided. 
- The logistic regression model is the best performing model with an accuracy of 91% on the training and test data.
- From the confusion matrix we can see that, out of 1290 positive sentiments present in the test data, it was able to correctly predict for 1171 positive sentiments, out of 757 neutral sentiments the model was able to correctly predict 651 neutral sentiments, and out of 1953 negative sentiments the model was able to correctly predict for 1816 sentiments.
