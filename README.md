# Sentimental-Analysis
Comparing two different sentiment analyzers, which are TextBlob and Vader. For both tools, we determine the results with positive, negative and neutral.

## Sentiment Analyzer - Textblob
In order to apply Textblob, we need to install the library first. We then use tweets as our input data to analyze the sentiment, which the data is already preprocessed. However, at this time we haven't integrated our code, so we decide to use dummy tweets first. We use built-in functions to get our polarity score. If the score is smaller than 0, it represents negative; if the score
is bigger than 0, it represents positive; else it represents neutral. After receiving the result, we can see the polarity and the sentiment of each tweet showing in the plot.

## Sentiment Analyzer - Vader
For Vader, we do the same thing as Textblob, installing the Vader library and calling the object "SentimentIntensityAnalyser". We can see that in Vader, it returns a form like a dictionary which indicates the compound score and the distribution of 'neg', 'neu' and 'pos'. The compound score is the same as the polarity score in Textblob. The computation of this score is based on summing the valence scores of each word in the lexicon. The threshold of the score at first depends on -0.05 and 0.05, however, it is normalized to be shown between -1 and 1 for easier representation.

## Comparison Between Tools & Problem Statement
In the result, we can see that most of the sentiment categories are the same. However, there's a little difference between the positive and negative. Through the observation, we think it's because Vader has better analysis with social media, since it can deal with emoticons. One of the challenges in sentiment analysis is that when setting the input data to Textblob and Vader, the data type cannot be series. Similarly, the datatypes of outputs with both tools are different, so we need to be aware of this part to prevent the errors from happening. Although we are stuck in this part for a while, we finally produce the result and the plots.
