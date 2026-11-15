---
title: Datasets
description: Sentiment analysis datasets and candidate data sources.
---

## Datasets we will use

## The following are potential datasets.  Have not been evaluated yet (Jeff) will look

- TweetEval sentiment - realistic short-form positive/neutral/negative language. Already has irony and sarcasm in it.  [TweetEval](https://huggingface.co/datasets/cardiffnlp/tweet_eval)
     - Tweeteval also has irony in it as a separate configuration
 
     **Analysis**
       - The irony config will not help us since it is testing for irony as a true/false condition, similar in how we test for positive/negative sentement.
       - The sentiment config provides a good dataset for sentiment analysis.  Not sure if it includes sarcasm or other mixed positive/negative statements, but does
              have labels that can be used for training.

  A sample of how to use the Tweeteval sentiment config dataset can be found at [TweetEval Notebook](https://github.com/NJIT-DS677-Deep-Learning/distilbert-sentiment-analysis/blob/main/samples/TweetEval_test.ipynb)
  
- Sarcasm Detection dataset - The Sarcasm Detection Dataset is designed for identifying instances of sarcasm in text. [Sarcasm Detection](https://huggingface.co/datasets/SarcasmNet/sarcasm)
     **Analysis**
       The scarcasm detection dataset is not usable since it only contains labels for sarcasm and not for sentiment analysis
  
- GoEmotions - introduce examples containing more complicated and overlapping emotional information.  This site also has code where they fine tuned a pre-trained BERT model.  [GoEmotions](https://github.com/google-research/google-research/blob/master/goemotions/README.md).  Go emotions has 27 different labels, but they provide a sentiment dictionary to group those emotion labels into positive, neutral, or negative sentiment.  A sentence can have more than one emotion label, so in the test notebook there is a vote for each label and the sentiment with the most votes wins.
     **Analysis**
       This dataset tests for 27 different labels and a sentence can have more than one label.  They provide a sentiment mapping file that maps emotions to sentiment analysis.  As a result we can use this dataset.  A sample of how to use this dataset and how to map it can be found in the [GOEmotions Notebook](https://github.com/NJIT-DS677-Deep-Learning/distilbert-sentiment-analysis/blob/main/samples/go_emotions.ipynb)
  
- BESSTIE - dataset includes both sentiment analysis AND sarcasm labels.  Only potential issue is that it's based on UK, Indian and Australian dialects of English.  There is also no neutral sentiment.  It's either positive or negative. [BESSTIE](https://huggingface.co/datasets/unswnlporg/BESSTIE).

     **Analysis**
       This dataset is unique in that unlike the other datasets it provides labels for both sentiment analysis and sarcasm allowing us to easily test sentiment analysis scenarios with sarcasm.

  A notebook showing how to use BESSTIE can be found at [BESTIE Notebook](https://github.com/NJIT-DS677-Deep-Learning/distilbert-sentiment-analysis/blob/main/samples/BESSTIE_test.ipynb)
