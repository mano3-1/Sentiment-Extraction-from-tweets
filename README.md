# Sentiment-Extraction-from-tweets
The main goal of this repository is to obtain the phrases or words from a given sentence which strongly agree to the corresponding sentiment. For a detailed information about the tweet sentiment extraction problem and XLNet I strongly suggest [this medium post](https://medium.com/analytics-vidhya/finetuning-a-xlnet-for-sentiment-extraction-9e75ded91f1c) written by me.
## What is sentiment extraction?
Sentiment extraction is natural language processing task where a sentence and it's corresponding sentiment(whether it is a positive or negaitve or neutral sentence) will be given and model is supposed to extract phrases or set of words which strongly support the given sentiment.
## About Data and Task
The data I used in this repository is from kaggle's [tweet sentiment extraction](https://www.kaggle.com/c/tweet-sentiment-extraction/data) challenge.<br/>
In each row ,it has text and corresponding sentiment and selected text.<br/>
The challenge is to learn a model to map text ,sentiment to selected text.

## Method:
We used transformer based models like ALBERT ,XLNET ,ROBERTA to with a CNN head on top.We trained these BERT models along with CNN head using a binary cross entropy model(with 0.1 label smoothing).We tried to predict the start and end indicies ,thereby obtaining the selected text.

## Training Strategy:
We used Stratified K-fold method to reduce the variance in the model.

##  About Metric:
Jacaard metric is used to evaluate the model.Jacaard metric is quiet similar to IOU in computer vision.To know more about the jaccard metric ,I strongly suggest you to take a look at this awesomely written [medium](https://towardsdatascience.com/overview-of-text-similarity-metrics-3397c4601f50) post.
## Results:
### XLNET RESULTS:
Negative : <br/>
 !["negative"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/xlnet1.PNG)<br/>
Positive : <br/>
 !["positive"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/xlnet2.PNG)<br/>
 !["positive"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/xlnet3.PNG)<br/>
Neutral : <br/>
 !["neutral"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/xlnet4.PNG)<br/>
 ### Roberta RESULTS:
 Negative : <br/>
 !["negative"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/roBERTa1.PNG)<br/>
Positive : <br/>
 !["positive"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/roBERTa2.PNG)<br/>
 !["positive"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/roBERTa3.PNG)<br/>
Neutral : <br/>
 !["neutral"](https://github.com/mano3-1/Sentiment-Extraction-from-tweets/blob/master/results/roBERTa4.PNG)<br/>
