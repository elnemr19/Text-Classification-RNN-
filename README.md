# Text-Classification-RNN-

## 1. Project Description

The goal of this project is to develop a deep learning model that can accurately classify text into one of seven categories: **tech**, **business**, **sport**, **entertainment**, and **politics**.

We will use **Long Short-Term Memory (LSTM)** to train our model, as they have been shown to be effective in understanding  sequence. Our approach involves training a LSTM model on the **BBC articles** dataset.


## 2. Table of Contents
[Dataset](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#3-dataset)

[Model Overview](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#4-model-overview)


[Results](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#5-results)

[Deployment](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#6-deployment)


## 3. Dataset

-Source : Kaggel - [BBC News](https://www.kaggle.com/datasets/yufengdev/bbc-fulltext-and-category) .

-Description :The data contain five classes (**tech**, **business**, **sport**, **entertainment**, and **politics** ).

![image](https://github.com/user-attachments/assets/b4f9b037-8da7-40f7-9d8b-3e635310f676)


## 4. Pre-processing

In this phase I:
remove the punctuation and stopwords and convert text to lower.
convert text into integer sequences by tokenizer, mapping each word to a unique index, and handles out-of-vocabulary words using a specified token (<OOV>).
pads or truncates these sequences to a fixed length, ensuring uniform input size for deep learning models.
word embedding:


## 4. Model Overview


## 5. Results

## 6. Deployment
