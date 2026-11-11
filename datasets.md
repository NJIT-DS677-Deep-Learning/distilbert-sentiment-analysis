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
  
- Sarcasm Detection dataset - The Sarcasm Detection Dataset is designed for identifying instances of sarcasm in text. [Sarcasm Detection](https://huggingface.co/datasets/SarcasmNet/sarcasm)
- GoEmotions - introduce examples containing more complicated and overlapping emotional information.  This site also has code where they fine tuned a pre-trained BERT model.  [GoEmotions](https://github.com/google-research/google-research/blob/master/goemotions/README.md)
- BESSTIE - dataset includes both sentiment analysis AND sarcasm labels.  Only potential issue is that it's based on UK, Indian and Australian dialects of English.  There is also no neutral sentiment.  It's either positive or negative. [BESSTIE](https://huggingface.co/datasets/unswnlporg/BESSTIE).  