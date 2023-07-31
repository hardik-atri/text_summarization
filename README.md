# Text Summarization

This project demonstrates the implementation of a Sequence-to-Sequence model for text summarization using the Amazon review dataset.

## Project Overview

This project aims to build a text summarization model using the Amazon review dataset. The model takes a text review as input and generates a summary of the review as output. The steps followed in this project are outlined below:

## Steps

1. **Load the Amazon Review Dataset**

   The first step involves loading the Amazon review dataset, which will be used for training and testing the summarization model.

2. **Data Cleaning**

   Data cleaning is performed to ensure the dataset is free from any duplicate entries or missing values (NaN).

3. **Text Preprocessing**

   The text review and summary are preprocessed to make them suitable for training the model. The following steps are applied:
   - Convert all text to lowercase.
   - Extract text within HTML tags, if any.
   - Remove text within parentheses.
   - Replace contractions like "can't" with "cannot."
   - Remove special characters from the text.

4. **Add Start and End Tokens**

   Start and End tokens are added to the summary text to indicate the beginning and end of the sequence during training.

5. **Analyze Review and Summary Length**

   The distribution of word counts in reviews and summaries is plotted to gain insights into the data.

6. **Data Split**

   The dataset is split into a training set and a test set to evaluate the model's performance.

7. **Tokenization**

   The input text and target summaries are tokenized to convert them into numerical sequences.

8. **Post-padding**

   Post-padding is applied to ensure all input sequences have the same length, making them suitable for training the model.

9. **Decoder Input and Target**

   For the input to the decoder, the "End of Sequence" token is removed, and for the target decoder, the "Start of Sequence" token is removed.

10. **Build Sequence-to-Sequence Model**

    The sequence-to-sequence model is constructed with the following components:
    - Encoder: Embedding layer, 3 LSTM layers.
    - Decoder: Embedding layer, 1 LSTM layer, attention layer, dense layer.
    - Categorical cross-entropy is used as the loss function.

11. **Also used transformer based model for this purpose**
