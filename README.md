# Final Project - text classification using Amazon Reviews dataset

## Description

This repository contains the files for the final project of Advanced Natural Language Processing course in winter term of 2023 of Barcelona School of Economics.

The dataset used for this work is available in [this link](https://huggingface.co/datasets/amazon_us_reviews).



## Baseline models

For the baseline models we applied a logistic regression. Surprisingly the best results were obtained by this simple model without any pre-processing, after we apply some pre processing

## Neural Network


## BERT

In this section we will develop a multi-class text classifier using BERT (Bidirectional Encoder Representations from Transformers), a Machine Learning model based on transformers², i.e. attention components able to learn contextual relations between words.

For the purpose of classification, we need numeric labels. Therefore, we map the topics descriptions to integers. Also, we make use of the bert_en_uncased_preprocess/L-12_H-768_A-12 model, a matching text preprocessing models and the pre-trained encoder provided by TensorFlow.
What we want to achieve is to turn text into high-dimensional vectors that capture sentence-level semantics. Therefore, we proceed by loading the preprocessor and the encoder layers from the endpoints provided by TensorFlow Hub and define a simple function to get the embeddings from input text.
As the model is based on the BERT transformer architecture, it will generate a pooled_output (output embedding of the entire sequence). 

As we are facing a multi-class classification problem, and we previously noticed that our topics distribution is highly imbalanced, we might want to observe different metrics during model training.

We initially split the dataset in train and test set, but we used both during the training and validation procedure.
In order to fairly estimate our performances, we evaluate the quality of the predictions on a new dataset containing observations that were not “seen” by the model during training (blind set).




## Credits

Supervisor: Arnault Gombert(https://github.com/agombert)

Collaborators:
- [Erika Gutierrez](https://github.com/erikaguti)
- Lucas Santos
- [Margherita Phillip]()
- [Renato Vassalo](https://github.com/RenatoVassallo)



## Limitations and future directions

This worked focused on the text classification task using a subset of the amazon reviews dataset. Our model presented bias ... Future directions could be using the whole dataset to train the model and trying to apply the same tasks to all the categories available, exposing the model to categories with high level of similarity and assess the perform of the model on it.

