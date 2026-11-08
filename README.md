# distilbert-sentiment-analysis
Test of DistilBERT using sentiment analysis

**Claim -** We claim that DistilBERT fine-tuned on SST-2 achieves higher sentiment classification accuracy than a TF-IDF + logistic regression baseline on the SST-2 validation set.

**Evaluation plan -** We will also test whether this advantage holds on data the models were not trained on. Both models will be trained on SST-2 and then evaluated on several other sentiment datasets. This shows whether fine-tuning on one dataset improves accuracy on data from other domains.

**Stress test -** We will also evaluate both models on a harder dataset. This dataset should include a mix of positive and negative sentiment within a single review, and include elements such as sarcasm that are designed to confuse a classifier.

**Upper bound -** Finally, we will run a sample from each dataset through current state-of-the-art industry models. Their accuracy gives an approximate upper limit on achievable performance.
