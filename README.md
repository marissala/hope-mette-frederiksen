# HOPE: Mentions of Mette Frederiksen in the Danish Twitter
This repository contains an overview of the discourse on the Danish Twitter in relation to the Danish prime minister Mette Frederiksen.

Data was collected with the following keywords:
- 'mettef', 'mettefrederiksen', 'mettefredriksen', 
- '#mettef', '#mettefrederiksen', '#mettefredriksen',
- 'mette frederiksen', 'mette fredriksen',
- '@statsmin'

The search checks for which keywords and keyword combinations are mentioned in a tweet. Overall, there are **28 393** matching tweets, with an average of **144.3** tweets per day.

## Date range
1.12.2020 until 22.01.2021

## Preprocessing
Retweets were discarded, and quote tweets were removed. The way of removal was via checking whether the 50 first characters overlapped between the tweets in the dataset (user mentions in the beginning of tweets were ignored). This resulted in the removal of 2236 duplicates.

## Time series analysis
![Time series of mentions](fig/tweet_frequency.png)
The above figure shows the total mentions of Mette Frederiksen together with the mentions of @Statsmin.

## Frequent hashtags
A hashtag analysis was conducted to see if there might be a trending hashtag popping up in the dataset.

![Frequent hashtags](fig/frequent_hashtags.png)
These are the 30 most popular hashtags used in the dataset. The most popular hashtags are popular hashtags related to Covid-19 - #dkpol, #covid19dk, #dkmedier. Thereafter hashtags like #mettefrederiksen together with mink-related hashtags show up.

## Sentiment analysis
The compound semantic scores were calculated with the Danish Vader.
![Sentiment analysis](fig/sentiment_compound.png)

Taking the monthly averages of compound sentiment shows that the average is always slightly positive, and the lowest it gets on average is in December 2020.
![Monthly sentiment average](fig/sentiment_compound_monthly.png)

## Word frequency
For the following analysis, all tweets were tokenized and lemmatized, stop words were removed.
![Word frequency](fig/word_frequency.png)

![Word cloud](fig/word_cloud.png)

## Bigram network analysis
A network-bigram analysis was conducted on the data to investigate which words co-occur. This enables the visualization of bi- and trigrams which the previous word frequency analysis neglects.
![Bigrams](fig/bigram_graph.png)
