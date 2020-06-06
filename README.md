# Sentiment-Extraction-from-tweets
The main goal of this repository is to obtain the phrases or words from a given sentence which strongly agree to the corresponding sentiment.
## What is sentiment extraction?
Sentiment extraction is natural language processing task where a sentence and it's corresponding sentiment(whether it is a positive or negaitve or neutral sentence) will be given and model is supposed to extract phrases or set of words which strongly support the given sentiment.
## About Data and Task
The data I used in this repository is from kaggle's [tweet sentiment extraction](https://www.kaggle.com/c/tweet-sentiment-extraction/data) challenge.<br/>
In each row ,it has text and corresponding sentiment and selected text.<br/>
The challenge is to learn a model to map text ,sentiment to selected text.

## Method:
We used transformer based models like ALBERT ,XLNET ,ROBERTA to with a CNN head on top.

## Results:
