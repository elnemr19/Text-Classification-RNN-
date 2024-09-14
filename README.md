# Text-Classification-RNN-

## 1. Project Description

The goal of this project is to develop a deep learning model that can accurately classify text into one of seven categories: **tech**, **business**, **sport**, **entertainment**, and **politics**.

We will use **Long Short-Term Memory (LSTM)** to train our model, as they have been shown to be effective in understanding  sequence. Our approach involves training a LSTM model on the **BBC articles** dataset.


## 2. Table of Contents
[Dataset](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#3-dataset)

[Pre-processing](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#4-pre-processing)

[Model Overview](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#4-model-overview)


[Results](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#5-results)

[Deployment](https://github.com/elnemr19/Text-Classification-RNN-/blob/main/README.md#6-deployment)


## 3. Dataset

-Source : Kaggel - [BBC News](https://www.kaggle.com/datasets/yufengdev/bbc-fulltext-and-category) .

-Description :The data contain five classes (**tech**, **business**, **sport**, **entertainment**, and **politics** ).

![image](https://github.com/user-attachments/assets/b4f9b037-8da7-40f7-9d8b-3e635310f676)


## 4. Pre-processing

In this phase I:

-remove the punctuation and stopwords and convert text to lower.

-convert text into integer sequences by tokenizer, mapping each word to a unique index, and handles out-of-vocabulary words using a specified token (<OOV>).

-pads or truncates these sequences to a fixed length, ensuring uniform input size for deep learning models.

-word embedding:
I used **GloVe** (Global Vectors for Word Representation) :is a pre-trained word embedding model where each word is represented as a vector of real numbers, capturing semantic meanings and relationships between words.

-I used LabelEncoder to encode the target (labels).

-Split my data into train and test by 80 - 20.

## 5. Model Overview
This model is a **Bidirectional LSTM-based sequential neural network** for multi-class classification with an output layer using the softmax activation function.
Key components include:

**Embedding Layer**: Initialized with pre-trained GloVe embeddings (non-trainable) to represent words as dense vectors.

**Bidirectional LSTMs**: Three stacked Bidirectional LSTM layers with 128, 64, and 32 units, respectively, to capture both forward and backward dependencies in the input sequences.

**Dropout Layers**: Dropout layers after each LSTM and Dense layer to prevent overfitting.

**Dense Layers**: Two fully connected layers—one with 64 units and ReLU activation, and the final layer with 5 units (softmax activation) for multi-class classification.

**Loss Function**: Uses sparse_categorical_crossentropy for multi-class classification.

**Optimizer**: Adam optimizer for efficient training.

**Early Stopping**: Implemented to monitor validation loss, with a patience of 3 epochs to prevent overfitting and restore the best weights.



## 6. Results
My final accuracy is 96% in traning ,92% in testing.

Accuracy:
![image](https://github.com/user-attachments/assets/15146026-48b6-432a-a0f6-6158286d5683)

Loss:
![image](https://github.com/user-attachments/assets/4a68b02e-d9c6-494c-8f33-8af2e8964663)

Confusion Matrix:
![image](https://github.com/user-attachments/assets/5e0e169b-3ec1-4b72-94e6-ce030f3febaa)

![image](https://github.com/user-attachments/assets/55f2174e-5e8e-4758-aae1-9b23921fdc52)


## 7. Deployment

I used gradio to make user interface


