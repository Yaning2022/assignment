**Research note**  
**Assignment:** Can we identify a model's learned behavior by examining its weights?  
**Author:** Yaning Wang  

---

### Abstract

This experiment investigates whether a model's learned language behaviour can be identified by examining its numerical weights alone. Two convolutional neural network (CNN) language models were trained using text. One model was trained on English text and the other on Swedish text.

The saved model weights were examined and presented to an AI assistant which is a normal ChatGPT in an anonymised format. Chatgpt was instructed to identify which model had been trained on which language, using only the numerical weights and without running the models or generating predictions.

Chatgpt could not identify either language from the weights alone. This result does not demonstrate that language information is absent from the weights. Instead, it suggests that identifying learned behaviour from raw weights may be difficult, particularly with small datasets and a limited experimental setup.

### Research question

**Can we identify a model's learned language behaviour by examining its weights alone?**
I use Chatgpt to identify whether a small CNN model was trained on English or Swedish by examining only its numerical weights. To investigate this question, I trained two small CNN language models. Both models used text about the same geographical topic, Norrköping, Sweden, but one was trained on English text and the other on Swedish text.

The experiment focuses on whether Chatgpt can distinguish the two models from their saved weights without executing either model.

### Hypothesis

My hypothesis was:

An AI assistant can identify whether a small CNN model learned English or Swedish by examining its trained weights alone.

### Design

Two character-level 1D CNN language models were trained:

| Model | Training language | Topic |
|---|---|---|
| Model A | English | Norrköping, Sweden |
| Model B | Swedish | Norrköping, Sweden |

Both models used the same general model architecture: a convolutional neural network.

The saved weight files were:

norrkoping_english_cnn.weights.h5
norrkoping_swedish_cnn.weights.h5

To investigate whether Chatgpt could identify the learned language, I prepared anonymised copies of the two weight files:

model_A.weights.h5, English dataset
model_B.weights.h5, Swedish dataset

The original filenames were hidden to avoid revealing the training language.

I uploaded the two files to Chatgpt and wrote the prompt


### Results

Its conclusion was:

"Based exclusively on the numerical weights provided, I cannot reliably identify Model A as English or Swedish, nor Model B. Assigning either language would amount to guessing rather than evidence-based identification."

Therefore, the initial experiment did not support the hypothesis.

### AI usage

ChatGPT, were used as supporting tools during this project. ChatGPT assisted with understanding the concept of weight-space programming, discussing the experimental design, troubleshooting Python code.

ChatGPT was also used to conduct a blind analysis of the anonymised model weight files to investigate whether the models could be identified as English-trained or Swedish-trained based only on their weights. 