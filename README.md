# App Review Sentiment Analysis (GoPay)
## Business Understanding
## The Objective
The objectives of this project are:
1. Collect and process the user review data of GoPay app.
2. Perform sentiment analysis to classify the user reviews into positive, negative, or neutral.
3. Build an accurate predictive model to predict the user sentiment based on their review text.

## Data Understanding
The data obtained through scraping technique of user review data for GoPay app on Google Playstore with (google play scraper)[https://pypi.org/project/google-play-scraper/] library. (Dataset)[]

## Text preprocessing
Text preprocessing techniques indclude: 
- Text cleaning (remove mentions, hashtags, links, digits, punctuations).
- Lower case.
- Tokenizing.
- Remove stopwords.
- Stemming.
- Remove slangwords.

## Labelling
Labelling process is done based on the user review, each word in the text of user review checked and given a score based on a dictionary of (positive)[https://github.com/angelmetanosaa/dataset/blob/main/lexicon_positive.csv] and (negative words)[https://github.com/angelmetanosaa/dataset/blob/main/lexicon_negative.csv], then the total score used as a reference to determine whether the text belongs to the positive, negative, or neutral sentiment category.

## Feature Extraction
The feature extraction used is TF-IDF.

## Modeling
Four models with different algorithms were compared to find the model with the best perfomance, the four algorithms are Naive Bayes, Random Forest, Logistic Regression, and Decision Tree.

## Evaluation
Of the four models, the logistic regression model has the best accuracy compared to other models, with 91% accuracy.

![Screenshot (987)](https://github.com/user-attachments/assets/eb5b96ea-977d-4d7b-ae54-fb092c7a3842)

![confusion matrix](https://github.com/user-attachments/assets/0dc90fb1-f281-4b2b-85ef-080ff894143c)

## Conclusion
- The logistic regression model is the best performing model with an accuracy of 91% on the training and test data.
- From the confusion matrix we can see that, out of 1290 positive sentiments present in the test data, it was able to correctly predict for 1171 positive sentiments, out of 757 neutral sentiments the model was able to correctly predict 651 neutral sentiments, and out of 1953 negative sentiments the model was able to correctly predict for 1816 sentiments.
