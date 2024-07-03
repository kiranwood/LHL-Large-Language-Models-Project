# LLM Project

## Important Notice

Due to issues I had with github I was not able to post the datasets/models into folders on github as I would have liked. The code is still there in the notebooks for someone to recreate with all the data/models saved.

## Project Task

This project goal is to create a sentiment analysis tool to interpret emotions on reviews on movies. It is made to recognize if the review is positive or negative. 

## Dataset

This dataset used for this project is the imdb dataset. It is for binary classification with two datasets, one for testing and one for training. There is also unsupervised unlabeled data for evaluating as well. Each dataset has 25,000 rows of data, with two columns one for text and another for labels.

Here is the link to the dataset:
https://huggingface.co/datasets/stanfordnlp/imdb

## Pre-trained Model

I chose multiple models for this project. One of the models I choose to test was SiEBERT - English-Language Sentiment Classification (https://huggingface.co/siebert/sentiment-roberta-large-english).
The other model I choose for my fine tuning and optimization was DistilBERT base model uncased (https://huggingface.co/distilbert/distilbert-base-uncased)

## Performance Metrics

The chosen metric to use for the entire project is F1. This is to keep all the testing results consistent throughout the project. F1 is great for evaluating the overall model.

It was found that the SiEBERT model did not do well with the dataset as it had an F1 score of `0`. This is because while it was correctly identifying some negative reviews it was not correctly identifying any positive reviews. Because of this low F1 score, it was decided to switch to another model for the fine tuning portion.

Where as with the DistilBERT model it had an overall score of around `0.9265` with the optimization making little change. This score shows that the model was doing pretty well.

## Hyperparameters

Due to each training for a model taking an hour to 2 hours of my time I was not able to test multiple different parameters as I would have liked. If I had more time for this project, this would be something I'd go into more.
The parameters I did change was adding a weight decay and warmup-steps. Although this did not significantly change the model at all.

## Final Model Link

If you wish to try the final model I created for yourself it can be found at this link:

https://huggingface.co/KiranWood/sentiment-analysis-model

